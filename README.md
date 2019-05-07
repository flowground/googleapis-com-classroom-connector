# ![LOGO](logo.png) Google Classroom **flow**ground Connector

## Description

A generated **flow**ground connector for the Google Classroom API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/classroom/v1/swagger.json<br/>
Generated at: 2019-05-07T17:41:16+03:00

## API Description

Manages classes, rosters, and invitations in Google Classroom.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Returns a list of courses that the requesting user is permitted to view,<br/>
> restricted to those that match the request. Returned courses are ordered by<br/>
> creation time, with the most recently created coming first.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` for access errors.<br/>
> * `INVALID_ARGUMENT` if the query argument is malformed.<br/>
> * `NOT_FOUND` if any users specified in the query arguments do not exist.

*Tags:* `courses`

#### Input Parameters
* `courseStates` - _optional_ - Restricts returned courses to those in one of the specified states
The default value is ACTIVE, ARCHIVED, PROVISIONED, DECLINED.
* `pageSize` - _optional_ - Maximum number of items to return. Zero or unspecified indicates that the
server may assign a maximum.

The server may return fewer than the specified number of results.
* `pageToken` - _optional_ - nextPageToken
value returned from a previous
list call,
indicating that the subsequent page of results should be returned.

The list request must be
otherwise identical to the one that resulted in this token.
* `studentId` - _optional_ - Restricts returned courses to those having a student with the specified
identifier. The identifier can be one of the following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* `teacherId` - _optional_ - Restricts returned courses to those having a teacher with the specified
identifier. The identifier can be one of the following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a course.<br/>
> <br/>
> The user specified in `ownerId` is the owner of the created course<br/>
> and added as a teacher.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to create<br/>
> courses or for access errors.<br/>
> * `NOT_FOUND` if the primary teacher is not a valid user.<br/>
> * `FAILED_PRECONDITION` if the course owner's account is disabled or for<br/>
> the following request errors:<br/>
>     * UserGroupsMembershipLimitReached<br/>
> * `ALREADY_EXISTS` if an alias was specified in the `id` and<br/>
> already exists.

*Tags:* `courses`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a list of aliases for a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> course or for access errors.<br/>
> * `NOT_FOUND` if the course does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - The identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `pageSize` - _optional_ - Maximum number of items to return. Zero or unspecified indicates that the
server may assign a maximum.

The server may return fewer than the specified number of results.
* `pageToken` - _optional_ - nextPageToken
value returned from a previous
list call,
indicating that the subsequent page of results should be returned.

The list request
must be otherwise identical to the one that resulted in this token.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates an alias for a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to create the<br/>
> alias or for access errors.<br/>
> * `NOT_FOUND` if the course does not exist.<br/>
> * `ALREADY_EXISTS` if the alias already exists.<br/>
> * `FAILED_PRECONDITION` if the alias requested does not make sense for the<br/>
>   requesting user or course (for example, if a user not in a domain<br/>
>   attempts to access a domain-scoped alias).

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course to alias.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes an alias of a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to remove the<br/>
> alias or for access errors.<br/>
> * `NOT_FOUND` if the alias does not exist.<br/>
> * `FAILED_PRECONDITION` if the alias requested does not make sense for the<br/>
>   requesting user or course (for example, if a user not in a domain<br/>
>   attempts to delete a domain-scoped alias).

*Tags:* `courses`

#### Input Parameters
* `alias` - _required_ - Alias to delete.
This may not be the Classroom-assigned identifier.
* `courseId` - _required_ - Identifier of the course whose alias should be deleted.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a list of announcements that the requester is permitted to view.<br/>
> <br/>
> Course students may only view `PUBLISHED` announcements. Course teachers<br/>
> and domain administrators may view all announcements.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access<br/>
> the requested course or for access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course does not exist.

*Tags:* `courses`

#### Input Parameters
* `announcementStates` - _optional_ - Restriction on the `state` of announcements returned.
If this argument is left unspecified, the default value is `PUBLISHED`.
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `orderBy` - _optional_ - Optional sort ordering for results. A comma-separated list of fields with
an optional sort direction keyword. Supported field is `updateTime`.
Supported direction keywords are `asc` and `desc`.
If not specified, `updateTime desc` is the default behavior.
Examples: `updateTime asc`, `updateTime`
* `pageSize` - _optional_ - Maximum number of items to return. Zero or unspecified indicates that the
server may assign a maximum.

The server may return fewer than the specified number of results.
* `pageToken` - _optional_ - nextPageToken
value returned from a previous
list call,
indicating that the subsequent page of results should be returned.

The list request
must be otherwise identical to the one that resulted in this token.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates an announcement.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course, create announcements in the requested course, share a<br/>
> Drive attachment, or for access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course does not exist.<br/>
> * `FAILED_PRECONDITION` for the following request error:<br/>
>     * AttachmentNotVisible

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes an announcement.<br/>
> <br/>
> This request must be made by the Developer Console project of the<br/>
> [OAuth client ID](https://support.google.com/cloud/answer/6158849) used to<br/>
> create the corresponding announcement item.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting developer project did not create<br/>
> the corresponding announcement, if the requesting user is not permitted<br/>
> to delete the requested course or for access errors.<br/>
> * `FAILED_PRECONDITION` if the requested announcement has already been<br/>
> deleted.<br/>
> * `NOT_FOUND` if no course exists with the requested ID.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `id` - _required_ - Identifier of the announcement to delete.
This identifier is a Classroom-assigned identifier.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns an announcement.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course or announcement, or for access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course or announcement does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `id` - _required_ - Identifier of the announcement.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates one or more fields of an announcement.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting developer project did not create<br/>
> the corresponding announcement or for access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `FAILED_PRECONDITION` if the requested announcement has already been<br/>
> deleted.<br/>
> * `NOT_FOUND` if the requested course or announcement does not exist

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `id` - _required_ - Identifier of the announcement.
* `updateMask` - _optional_ - Mask that identifies which fields on the announcement to update.
This field is required to do an update. The update fails if invalid
fields are specified. If a field supports empty values, it can be cleared
by specifying it in the update mask and not in the Announcement object. If
a field that does not support empty values is included in the update mask
and not set in the Announcement object, an `INVALID_ARGUMENT` error will be
returned.

The following fields may be specified by teachers:

* `text`
* `state`
* `scheduled_time`
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Modifies assignee mode and options of an announcement.<br/>
> <br/>
> Only a teacher of the course that contains the announcement may<br/>
> call this method.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course or course work or for access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course or course work does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `id` - _required_ - Identifier of the announcement.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a list of course work that the requester is permitted to view.<br/>
> <br/>
> Course students may only view `PUBLISHED` course work. Course teachers<br/>
> and domain administrators may view all course work.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access<br/>
> the requested course or for access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `courseWorkStates` - _optional_ - Restriction on the work status to return. Only courseWork that matches
is returned. If unspecified, items with a work status of `PUBLISHED`
is returned.
* `orderBy` - _optional_ - Optional sort ordering for results. A comma-separated list of fields with
an optional sort direction keyword. Supported fields are `updateTime`
and `dueDate`. Supported direction keywords are `asc` and `desc`.
If not specified, `updateTime desc` is the default behavior.
Examples: `dueDate asc,updateTime desc`, `updateTime,dueDate desc`
* `pageSize` - _optional_ - Maximum number of items to return. Zero or unspecified indicates that the
server may assign a maximum.

The server may return fewer than the specified number of results.
* `pageToken` - _optional_ - nextPageToken
value returned from a previous
list call,
indicating that the subsequent page of results should be returned.

The list request
must be otherwise identical to the one that resulted in this token.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates course work.<br/>
> <br/>
> The resulting course work (and corresponding student submissions) are<br/>
> associated with the Developer Console project of the<br/>
> [OAuth client ID](https://support.google.com/cloud/answer/6158849) used to<br/>
> make the request. Classroom API requests to modify course work and student<br/>
> submissions must be made with an OAuth client ID from the associated<br/>
> Developer Console project.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course, create course work in the requested course, share a<br/>
> Drive attachment, or for access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course does not exist.<br/>
> * `FAILED_PRECONDITION` for the following request error:<br/>
>     * AttachmentNotVisible

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a list of student submissions that the requester is permitted to<br/>
> view, factoring in the OAuth scopes of the request.<br/>
> `-` may be specified as the `course_work_id` to include student<br/>
> submissions for multiple course work items.<br/>
> <br/>
> Course students may only view their own work. Course teachers<br/>
> and domain administrators may view all student submissions.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course or course work, or for access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `courseWorkId` - _required_ - Identifier of the student work to request.
This may be set to the string literal `"-"` to request student work for
all course work in the specified course.
* `late` - _optional_ - Requested lateness value. If specified, returned student submissions are
restricted by the requested value.
If unspecified, submissions are returned regardless of `late` value.
    Possible values: LATE_VALUES_UNSPECIFIED, LATE_ONLY, NOT_LATE_ONLY.
* `pageSize` - _optional_ - Maximum number of items to return. Zero or unspecified indicates that the
server may assign a maximum.

The server may return fewer than the specified number of results.
* `pageToken` - _optional_ - nextPageToken
value returned from a previous
list call,
indicating that the subsequent page of results should be returned.

The list request
must be otherwise identical to the one that resulted in this token.
* `states` - _optional_ - Requested submission states. If specified, returned student submissions
match one of the specified submission states.
* `userId` - _optional_ - Optional argument to restrict returned student work to those owned by the
student with the specified identifier. The identifier can be one of the
following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a student submission.<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course, course work, or student submission or for<br/>
> access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course, course work, or student submission<br/>
> does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `courseWorkId` - _required_ - Identifier of the course work.
* `id` - _required_ - Identifier of the student submission.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates one or more fields of a student submission.<br/>
> <br/>
> See google.classroom.v1.StudentSubmission for details<br/>
> of which fields may be updated and who may change them.<br/>
> <br/>
> This request must be made by the Developer Console project of the<br/>
> [OAuth client ID](https://support.google.com/cloud/answer/6158849) used to<br/>
> create the corresponding course work item.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting developer project did not create<br/>
> the corresponding course work, if the user is not permitted to make the<br/>
> requested modification to the student submission, or for<br/>
> access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course, course work, or student submission<br/>
> does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `courseWorkId` - _required_ - Identifier of the course work.
* `id` - _required_ - Identifier of the student submission.
* `updateMask` - _optional_ - Mask that identifies which fields on the student submission to update.
This field is required to do an update. The update fails if invalid
fields are specified.

The following fields may be specified by teachers:

* `draft_grade`
* `assigned_grade`
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Modifies attachments of student submission.<br/>
> <br/>
> Attachments may only be added to student submissions belonging to course<br/>
> work objects with a `workType` of `ASSIGNMENT`.<br/>
> <br/>
> This request must be made by the Developer Console project of the<br/>
> [OAuth client ID](https://support.google.com/cloud/answer/6158849) used to<br/>
> create the corresponding course work item.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course or course work, if the user is not permitted to modify<br/>
> attachments on the requested student submission, or for<br/>
> access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course, course work, or student submission<br/>
> does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `courseWorkId` - _required_ - Identifier of the course work.
* `id` - _required_ - Identifier of the student submission.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Reclaims a student submission on behalf of the student that owns it.<br/>
> <br/>
> Reclaiming a student submission transfers ownership of attached Drive<br/>
> files to the student and updates the submission state.<br/>
> <br/>
> Only the student that owns the requested student submission may call this<br/>
> method, and only for a student submission that has been turned in.<br/>
> <br/>
> This request must be made by the Developer Console project of the<br/>
> [OAuth client ID](https://support.google.com/cloud/answer/6158849) used to<br/>
> create the corresponding course work item.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course or course work, unsubmit the requested student submission,<br/>
> or for access errors.<br/>
> * `FAILED_PRECONDITION` if the student submission has not been turned in.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course, course work, or student submission<br/>
> does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `courseWorkId` - _required_ - Identifier of the course work.
* `id` - _required_ - Identifier of the student submission.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a student submission.<br/>
> <br/>
> Returning a student submission transfers ownership of attached Drive<br/>
> files to the student and may also update the submission state.<br/>
> Unlike the Classroom application, returning a student submission does not<br/>
> set assignedGrade to the draftGrade value.<br/>
> <br/>
> Only a teacher of the course that contains the requested student submission<br/>
> may call this method.<br/>
> <br/>
> This request must be made by the Developer Console project of the<br/>
> [OAuth client ID](https://support.google.com/cloud/answer/6158849) used to<br/>
> create the corresponding course work item.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course or course work, return the requested student submission,<br/>
> or for access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course, course work, or student submission<br/>
> does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `courseWorkId` - _required_ - Identifier of the course work.
* `id` - _required_ - Identifier of the student submission.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Turns in a student submission.<br/>
> <br/>
> Turning in a student submission transfers ownership of attached Drive<br/>
> files to the teacher and may also update the submission state.<br/>
> <br/>
> This may only be called by the student that owns the specified student<br/>
> submission.<br/>
> <br/>
> This request must be made by the Developer Console project of the<br/>
> [OAuth client ID](https://support.google.com/cloud/answer/6158849) used to<br/>
> create the corresponding course work item.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course or course work, turn in the requested student submission,<br/>
> or for access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course, course work, or student submission<br/>
> does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `courseWorkId` - _required_ - Identifier of the course work.
* `id` - _required_ - Identifier of the student submission.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes a course work.<br/>
> <br/>
> This request must be made by the Developer Console project of the<br/>
> [OAuth client ID](https://support.google.com/cloud/answer/6158849) used to<br/>
> create the corresponding course work item.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting developer project did not create<br/>
> the corresponding course work, if the requesting user is not permitted<br/>
> to delete the requested course or for access errors.<br/>
> * `FAILED_PRECONDITION` if the requested course work has already been<br/>
> deleted.<br/>
> * `NOT_FOUND` if no course exists with the requested ID.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `id` - _required_ - Identifier of the course work to delete.
This identifier is a Classroom-assigned identifier.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns course work.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course or course work, or for access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course or course work does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `id` - _required_ - Identifier of the course work.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates one or more fields of a course work.<br/>
> <br/>
> See google.classroom.v1.CourseWork for details<br/>
> of which fields may be updated and who may change them.<br/>
> <br/>
> This request must be made by the Developer Console project of the<br/>
> [OAuth client ID](https://support.google.com/cloud/answer/6158849) used to<br/>
> create the corresponding course work item.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting developer project did not create<br/>
> the corresponding course work, if the user is not permitted to make the<br/>
> requested modification to the student submission, or for<br/>
> access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `FAILED_PRECONDITION` if the requested course work has already been<br/>
> deleted.<br/>
> * `NOT_FOUND` if the requested course, course work, or student submission<br/>
> does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `id` - _required_ - Identifier of the course work.
* `updateMask` - _optional_ - Mask that identifies which fields on the course work to update.
This field is required to do an update. The update fails if invalid
fields are specified. If a field supports empty values, it can be cleared
by specifying it in the update mask and not in the CourseWork object. If a
field that does not support empty values is included in the update mask and
not set in the CourseWork object, an `INVALID_ARGUMENT` error will be
returned.

The following fields may be specified by teachers:

* `title`
* `description`
* `state`
* `due_date`
* `due_time`
* `max_points`
* `scheduled_time`
* `submission_modification_mode`
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Modifies assignee mode and options of a coursework.<br/>
> <br/>
> Only a teacher of the course that contains the coursework may<br/>
> call this method.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course or course work or for access errors.<br/>
> * `INVALID_ARGUMENT` if the request is malformed.<br/>
> * `NOT_FOUND` if the requested course or course work does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `id` - _required_ - Identifier of the coursework.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a list of students of this course that the requester<br/>
> is permitted to view.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `NOT_FOUND` if the course does not exist.<br/>
> * `PERMISSION_DENIED` for access errors.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `pageSize` - _optional_ - Maximum number of items to return. Zero means no maximum.

The server may return fewer than the specified number of results.
* `pageToken` - _optional_ - nextPageToken
value returned from a previous
list call, indicating that
the subsequent page of results should be returned.

The list request must be
otherwise identical to the one that resulted in this token.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Adds a user as a student of a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to create<br/>
> students in this course or for access errors.<br/>
> * `NOT_FOUND` if the requested course ID does not exist.<br/>
> * `FAILED_PRECONDITION` if the requested user's account is disabled,<br/>
> for the following request errors:<br/>
>     * CourseMemberLimitReached<br/>
>     * CourseNotModifiable<br/>
>     * UserGroupsMembershipLimitReached<br/>
> * `ALREADY_EXISTS` if the user is already a student or teacher in the<br/>
> course.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course to create the student in.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `enrollmentCode` - _optional_ - Enrollment code of the course to create the student in.
This code is required if userId
corresponds to the requesting user; it may be omitted if the requesting
user has administrative permissions to create students for any user.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes a student of a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to delete<br/>
> students of this course or for access errors.<br/>
> * `NOT_FOUND` if no student of this course has the requested ID or if the<br/>
> course does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `userId` - _required_ - Identifier of the student to delete. The identifier can be one of the
following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a student of a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to view<br/>
> students of this course or for access errors.<br/>
> * `NOT_FOUND` if no student of this course has the requested ID or if the<br/>
> course does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `userId` - _required_ - Identifier of the student to return. The identifier can be one of the
following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a list of teachers of this course that the requester<br/>
> is permitted to view.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `NOT_FOUND` if the course does not exist.<br/>
> * `PERMISSION_DENIED` for access errors.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `pageSize` - _optional_ - Maximum number of items to return. Zero means no maximum.

The server may return fewer than the specified number of results.
* `pageToken` - _optional_ - nextPageToken
value returned from a previous
list call, indicating that
the subsequent page of results should be returned.

The list request must be
otherwise identical to the one that resulted in this token.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a teacher of a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not  permitted to create<br/>
> teachers in this course or for access errors.<br/>
> * `NOT_FOUND` if the requested course ID does not exist.<br/>
> * `FAILED_PRECONDITION` if the requested user's account is disabled,<br/>
> for the following request errors:<br/>
>     * CourseMemberLimitReached<br/>
>     * CourseNotModifiable<br/>
>     * CourseTeacherLimitReached<br/>
>     * UserGroupsMembershipLimitReached<br/>
> * `ALREADY_EXISTS` if the user is already a teacher or student in the<br/>
> course.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes a teacher of a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to delete<br/>
> teachers of this course or for access errors.<br/>
> * `NOT_FOUND` if no teacher of this course has the requested ID or if the<br/>
> course does not exist.<br/>
> * `FAILED_PRECONDITION` if the requested ID belongs to the primary teacher<br/>
> of this course.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `userId` - _required_ - Identifier of the teacher to delete. The identifier can be one of the
following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a teacher of a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to view<br/>
> teachers of this course or for access errors.<br/>
> * `NOT_FOUND` if no teacher of this course has the requested ID or if the<br/>
> course does not exist.

*Tags:* `courses`

#### Input Parameters
* `courseId` - _required_ - Identifier of the course.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `userId` - _required_ - Identifier of the teacher to return. The identifier can be one of the
following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to delete the<br/>
> requested course or for access errors.<br/>
> * `NOT_FOUND` if no course exists with the requested ID.

*Tags:* `courses`

#### Input Parameters
* `id` - _required_ - Identifier of the course to delete.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access the<br/>
> requested course or for access errors.<br/>
> * `NOT_FOUND` if no course exists with the requested ID.

*Tags:* `courses`

#### Input Parameters
* `id` - _required_ - Identifier of the course to return.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates one or more fields in a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to modify the<br/>
> requested course or for access errors.<br/>
> * `NOT_FOUND` if no course exists with the requested ID.<br/>
> * `INVALID_ARGUMENT` if invalid fields are specified in the update mask or<br/>
> if no update mask is supplied.<br/>
> * `FAILED_PRECONDITION` for the following request errors:<br/>
>     * CourseNotModifiable

*Tags:* `courses`

#### Input Parameters
* `id` - _required_ - Identifier of the course to update.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `updateMask` - _optional_ - Mask that identifies which fields on the course to update.
This field is required to do an update. The update will fail if invalid
fields are specified. The following fields are valid:

* `name`
* `section`
* `descriptionHeading`
* `description`
* `room`
* `courseState`
* `ownerId`

Note: patches to ownerId are treated as being effective immediately, but in
practice it may take some time for the ownership transfer of all affected
resources to complete.

When set in a query parameter, this field should be specified as

`updateMask=<field1>,<field2>,...`
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates a course.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to modify the<br/>
> requested course or for access errors.<br/>
> * `NOT_FOUND` if no course exists with the requested ID.<br/>
> * `FAILED_PRECONDITION` for the following request errors:<br/>
>     * CourseNotModifiable

*Tags:* `courses`

#### Input Parameters
* `id` - _required_ - Identifier of the course to update.
This identifier can be either the Classroom-assigned identifier or an
alias.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a list of invitations that the requesting user is permitted to<br/>
> view, restricted to those that match the list request.<br/>
> <br/>
> *Note:* At least one of `user_id` or `course_id` must be supplied. Both<br/>
> fields can be supplied.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` for access errors.

*Tags:* `invitations`

#### Input Parameters
* `courseId` - _optional_ - Restricts returned invitations to those for a course with the specified
identifier.
* `pageSize` - _optional_ - Maximum number of items to return. Zero means no maximum.

The server may return fewer than the specified number of results.
* `pageToken` - _optional_ - nextPageToken
value returned from a previous
list call, indicating
that the subsequent page of results should be returned.

The list request must be
otherwise identical to the one that resulted in this token.
* `userId` - _optional_ - Restricts returned invitations to those for a specific user. The identifier
can be one of the following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates an invitation. Only one invitation for a user and course may exist<br/>
> at a time. Delete and re-create an invitation to make changes.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to create<br/>
> invitations for this course or for access errors.<br/>
> * `NOT_FOUND` if the course or the user does not exist.<br/>
> * `FAILED_PRECONDITION` if the requested user's account is disabled or if<br/>
> the user already has this role or a role with greater permissions.<br/>
> * `ALREADY_EXISTS` if an invitation for the specified user and course<br/>
> already exists.

*Tags:* `invitations`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes an invitation.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to delete the<br/>
> requested invitation or for access errors.<br/>
> * `NOT_FOUND` if no invitation exists with the requested ID.

*Tags:* `invitations`

#### Input Parameters
* `id` - _required_ - Identifier of the invitation to delete.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns an invitation.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to view the<br/>
> requested invitation or for access errors.<br/>
> * `NOT_FOUND` if no invitation exists with the requested ID.

*Tags:* `invitations`

#### Input Parameters
* `id` - _required_ - Identifier of the invitation to return.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Accepts an invitation, removing it and adding the invited user to the<br/>
> teachers or students (as appropriate) of the specified course. Only the<br/>
> invited user may accept an invitation.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to accept the<br/>
> requested invitation or for access errors.<br/>
> * `FAILED_PRECONDITION` for the following request errors:<br/>
>     * CourseMemberLimitReached<br/>
>     * CourseNotModifiable<br/>
>     * CourseTeacherLimitReached<br/>
>     * UserGroupsMembershipLimitReached<br/>
> * `NOT_FOUND` if no invitation exists with the requested ID.

*Tags:* `invitations`

#### Input Parameters
* `id` - _required_ - Identifier of the invitation to accept.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a `Registration`, causing Classroom to start sending notifications<br/>
> from the provided `feed` to the destination provided in `cloudPubSubTopic`.<br/>
> <br/>
> Returns the created `Registration`. Currently, this will be the same as<br/>
> the argument, but with server-assigned fields such as `expiry_time` and<br/>
> `id` filled in.<br/>
> <br/>
> Note that any value specified for the `expiry_time` or `id` fields will be<br/>
> ignored.<br/>
> <br/>
> While Classroom may validate the `cloudPubSubTopic` and return errors on a<br/>
> best effort basis, it is the caller's responsibility to ensure that it<br/>
> exists and that Classroom has permission to publish to it.<br/>
> <br/>
> This method may return the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if:<br/>
>     * the authenticated user does not have permission to receive<br/>
>       notifications from the requested field; or<br/>
>     * the credential provided does not include the appropriate scope for<br/>
>       the requested feed.<br/>
>     * another access error is encountered.<br/>
> * `INVALID_ARGUMENT` if:<br/>
>     * no `cloudPubsubTopic` is specified, or the specified<br/>
>       `cloudPubsubTopic` is not valid; or<br/>
>     * no `feed` is specified, or the specified `feed` is not valid.<br/>
> * `NOT_FOUND` if:<br/>
>     * the specified `feed` cannot be located, or the requesting user does<br/>
>       not have permission to determine whether or not it exists; or<br/>
>     * the specified `cloudPubsubTopic` cannot be located, or Classroom has<br/>
>       not been granted permission to publish to it.

*Tags:* `registrations`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes a `Registration`, causing Classroom to stop sending notifications<br/>
> for that `Registration`.

*Tags:* `registrations`

#### Input Parameters
* `registrationId` - _required_ - The `registration_id` of the `Registration` to be deleted.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a list of guardian invitations that the requesting user is<br/>
> permitted to view, filtered by the parameters provided.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if a `student_id` is specified, and the requesting<br/>
>   user is not permitted to view guardian invitations for that student, if<br/>
>   `"-"` is specified as the `student_id` and the user is not a domain<br/>
>   administrator, if guardians are not enabled for the domain in question,<br/>
>   or for other access errors.<br/>
> * `INVALID_ARGUMENT` if a `student_id` is specified, but its format cannot<br/>
>   be recognized (it is not an email address, nor a `student_id` from the<br/>
>   API, nor the literal string `me`). May also be returned if an invalid<br/>
>   `page_token` or `state` is provided.<br/>
> * `NOT_FOUND` if a `student_id` is specified, and its format can be<br/>
>   recognized, but Classroom has no record of that student.

*Tags:* `userProfiles`

#### Input Parameters
* `invitedEmailAddress` - _optional_ - If specified, only results with the specified `invited_email_address`
will be returned.
* `pageSize` - _optional_ - Maximum number of items to return. Zero or unspecified indicates that the
server may assign a maximum.

The server may return fewer than the specified number of results.
* `pageToken` - _optional_ - nextPageToken
value returned from a previous
list call,
indicating that the subsequent page of results should be returned.

The list request
must be otherwise identical to the one that resulted in this token.
* `states` - _optional_ - If specified, only results with the specified `state` values will be
returned. Otherwise, results with a `state` of `PENDING` will be returned.
* `studentId` - _required_ - The ID of the student whose guardian invitations are to be returned.
The identifier can be one of the following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* the string literal `"-"`, indicating that results should be returned for
  all students that the requesting user is permitted to view guardian
  invitations.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a guardian invitation, and sends an email to the guardian asking<br/>
> them to confirm that they are the student's guardian.<br/>
> <br/>
> Once the guardian accepts the invitation, their `state` will change to<br/>
> `COMPLETED` and they will start receiving guardian notifications. A<br/>
> `Guardian` resource will also be created to represent the active guardian.<br/>
> <br/>
> The request object must have the `student_id` and<br/>
> `invited_email_address` fields set. Failing to set these fields, or<br/>
> setting any other fields in the request, will result in an error.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the current user does not have permission to<br/>
>   manage guardians, if the guardian in question has already rejected<br/>
>   too many requests for that student, if guardians are not enabled for the<br/>
>   domain in question, or for other access errors.<br/>
> * `RESOURCE_EXHAUSTED` if the student or guardian has exceeded the guardian<br/>
>   link limit.<br/>
> * `INVALID_ARGUMENT` if the guardian email address is not valid (for<br/>
>   example, if it is too long), or if the format of the student ID provided<br/>
>   cannot be recognized (it is not an email address, nor a `user_id` from<br/>
>   this API). This error will also be returned if read-only fields are set,<br/>
>   or if the `state` field is set to to a value other than `PENDING`.<br/>
> * `NOT_FOUND` if the student ID provided is a valid student ID, but<br/>
>   Classroom has no record of that student.<br/>
> * `ALREADY_EXISTS` if there is already a pending guardian invitation for<br/>
>   the student and `invited_email_address` provided, or if the provided<br/>
>   `invited_email_address` matches the Google account of an existing<br/>
>   `Guardian` for this user.

*Tags:* `userProfiles`

#### Input Parameters
* `studentId` - _required_ - ID of the student (in standard format)
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a specific guardian invitation.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to view<br/>
>   guardian invitations for the student identified by the `student_id`, if<br/>
>   guardians are not enabled for the domain in question, or for other<br/>
>   access errors.<br/>
> * `INVALID_ARGUMENT` if a `student_id` is specified, but its format cannot<br/>
>   be recognized (it is not an email address, nor a `student_id` from the<br/>
>   API, nor the literal string `me`).<br/>
> * `NOT_FOUND` if Classroom cannot find any record of the given student or<br/>
>   `invitation_id`. May also be returned if the student exists, but the<br/>
>   requesting user does not have access to see that student.

*Tags:* `userProfiles`

#### Input Parameters
* `invitationId` - _required_ - The `id` field of the `GuardianInvitation` being requested.
* `studentId` - _required_ - The ID of the student whose guardian invitation is being requested.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Modifies a guardian invitation.<br/>
> <br/>
> Currently, the only valid modification is to change the `state` from<br/>
> `PENDING` to `COMPLETE`. This has the effect of withdrawing the invitation.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the current user does not have permission to<br/>
>   manage guardians, if guardians are not enabled for the domain in question<br/>
>   or for other access errors.<br/>
> * `FAILED_PRECONDITION` if the guardian link is not in the `PENDING` state.<br/>
> * `INVALID_ARGUMENT` if the format of the student ID provided<br/>
>   cannot be recognized (it is not an email address, nor a `user_id` from<br/>
>   this API), or if the passed `GuardianInvitation` has a `state` other than<br/>
>   `COMPLETE`, or if it modifies fields other than `state`.<br/>
> * `NOT_FOUND` if the student ID provided is a valid student ID, but<br/>
>   Classroom has no record of that student, or if the `id` field does not<br/>
>   refer to a guardian invitation known to Classroom.

*Tags:* `userProfiles`

#### Input Parameters
* `invitationId` - _required_ - The `id` field of the `GuardianInvitation` to be modified.
* `studentId` - _required_ - The ID of the student whose guardian invitation is to be modified.
* `updateMask` - _optional_ - Mask that identifies which fields on the course to update.
This field is required to do an update. The update will fail if invalid
fields are specified. The following fields are valid:

* `state`

When set in a query parameter, this field should be specified as

`updateMask=<field1>,<field2>,...`
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a list of guardians that the requesting user is permitted to<br/>
> view, restricted to those that match the request.<br/>
> <br/>
> To list guardians for any student that the requesting user may view<br/>
> guardians for, use the literal character `-` for the student ID.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if a `student_id` is specified, and the requesting<br/>
>   user is not permitted to view guardian information for that student, if<br/>
>   `"-"` is specified as the `student_id` and the user is not a domain<br/>
>   administrator, if guardians are not enabled for the domain in question,<br/>
>   if the `invited_email_address` filter is set by a user who is not a<br/>
>   domain administrator, or for other access errors.<br/>
> * `INVALID_ARGUMENT` if a `student_id` is specified, but its format cannot<br/>
>   be recognized (it is not an email address, nor a `student_id` from the<br/>
>   API, nor the literal string `me`). May also be returned if an invalid<br/>
>   `page_token` is provided.<br/>
> * `NOT_FOUND` if a `student_id` is specified, and its format can be<br/>
>   recognized, but Classroom has no record of that student.

*Tags:* `userProfiles`

#### Input Parameters
* `invitedEmailAddress` - _optional_ - Filter results by the email address that the original invitation was sent
to, resulting in this guardian link.
This filter can only be used by domain administrators.
* `pageSize` - _optional_ - Maximum number of items to return. Zero or unspecified indicates that the
server may assign a maximum.

The server may return fewer than the specified number of results.
* `pageToken` - _optional_ - nextPageToken
value returned from a previous
list call,
indicating that the subsequent page of results should be returned.

The list request
must be otherwise identical to the one that resulted in this token.
* `studentId` - _required_ - Filter results by the student who the guardian is linked to.
The identifier can be one of the following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* the string literal `"-"`, indicating that results should be returned for
  all students that the requesting user has access to view.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes a guardian.<br/>
> <br/>
> The guardian will no longer receive guardian notifications and the guardian<br/>
> will no longer be accessible via the API.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if no user that matches the provided `student_id`<br/>
>   is visible to the requesting user, if the requesting user is not<br/>
>   permitted to manage guardians for the student identified by the<br/>
>   `student_id`, if guardians are not enabled for the domain in question,<br/>
>   or for other access errors.<br/>
> * `INVALID_ARGUMENT` if a `student_id` is specified, but its format cannot<br/>
>   be recognized (it is not an email address, nor a `student_id` from the<br/>
>   API).<br/>
> * `NOT_FOUND` if the requesting user is permitted to modify guardians for<br/>
>   the requested `student_id`, but no `Guardian` record exists for that<br/>
>   student with the provided `guardian_id`.

*Tags:* `userProfiles`

#### Input Parameters
* `guardianId` - _required_ - The `id` field from a `Guardian`.
* `studentId` - _required_ - The student whose guardian is to be deleted. One of the following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a specific guardian.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if no user that matches the provided `student_id`<br/>
>   is visible to the requesting user, if the requesting user is not<br/>
>   permitted to view guardian information for the student identified by the<br/>
>   `student_id`, if guardians are not enabled for the domain in question,<br/>
>   or for other access errors.<br/>
> * `INVALID_ARGUMENT` if a `student_id` is specified, but its format cannot<br/>
>   be recognized (it is not an email address, nor a `student_id` from the<br/>
>   API, nor the literal string `me`).<br/>
> * `NOT_FOUND` if the requesting user is permitted to view guardians for<br/>
>   the requested `student_id`, but no `Guardian` record exists for that<br/>
>   student that matches the provided `guardian_id`.

*Tags:* `userProfiles`

#### Input Parameters
* `guardianId` - _required_ - The `id` field from a `Guardian`.
* `studentId` - _required_ - The student whose guardian is being requested. One of the following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a user profile.<br/>
> <br/>
> This method returns the following error codes:<br/>
> <br/>
> * `PERMISSION_DENIED` if the requesting user is not permitted to access<br/>
> this user profile, if no profile exists with the requested ID, or for<br/>
> access errors.

*Tags:* `userProfiles`

#### Input Parameters
* `userId` - _required_ - Identifier of the profile to return. The identifier can be one of the
following:

* the numeric identifier for the user
* the email address of the user
* the string literal `"me"`, indicating the requesting user
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-classroom-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
