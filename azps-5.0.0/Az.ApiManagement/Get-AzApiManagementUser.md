---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 44f351870e97d227484bd09be1e75b8cb19ac723
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199927"
---
# <span data-ttu-id="a0a2d-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a0a2d-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="a0a2d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a2d-103">Ottiene un utente o utenti.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-103">Gets a user or users.</span></span>

## <span data-ttu-id="a0a2d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0a2d-104">SYNTAX</span></span>

### <span data-ttu-id="a0a2d-105">GeAllUsers (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0a2d-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0a2d-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="a0a2d-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0a2d-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="a0a2d-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0a2d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0a2d-108">DESCRIPTION</span></span>
<span data-ttu-id="a0a2d-109">Il cmdlet **Get-AzApiManagementUser** ottiene un utente specificato o tutti gli utenti, se non è specificato alcun utente.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="a0a2d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0a2d-110">EXAMPLES</span></span>

### <span data-ttu-id="a0a2d-111">Esempio 1: ottenere tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="a0a2d-111">Example 1: Get all users</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="a0a2d-112">Questo comando consente di ottenere tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-112">This command gets all users.</span></span>

### <span data-ttu-id="a0a2d-113">Esempio 2: ottenere un utente tramite ID</span><span class="sxs-lookup"><span data-stu-id="a0a2d-113">Example 2: Get a user by ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="a0a2d-114">Questo comando consente di ottenere un utente in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="a0a2d-115">Esempio 3: ottenere gli utenti in base al cognome</span><span class="sxs-lookup"><span data-stu-id="a0a2d-115">Example 3: Get users by last name</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="a0a2d-116">Questo comando ottiene gli utenti con un cognome specificato, Fuller.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="a0a2d-117">Esempio 4: ottenere un utente tramite indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="a0a2d-117">Example 4: Get a user by email address</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="a0a2d-118">Questo comando consente di ottenere l'utente con l'indirizzo di posta elettronica specificato.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="a0a2d-119">Esempio 5: ottenere tutti gli utenti all'interno di un gruppo</span><span class="sxs-lookup"><span data-stu-id="a0a2d-119">Example 5: Get all users within a group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="a0a2d-120">Questo comando consente di ottenere tutti gli utenti all'interno del gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="a0a2d-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0a2d-121">PARAMETERS</span></span>

### <span data-ttu-id="a0a2d-122">-Contesto</span><span class="sxs-lookup"><span data-stu-id="a0a2d-122">-Context</span></span>
<span data-ttu-id="a0a2d-123">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a2d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a2d-124">-DefaultProfile</span></span>
<span data-ttu-id="a0a2d-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a2d-126">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="a0a2d-126">-Email</span></span>
<span data-ttu-id="a0a2d-127">Specifica l'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="a0a2d-128">Se questo parametro viene specificato, questo cmdlet trova un utente tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="a0a2d-129">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-129">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a2d-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="a0a2d-130">-FirstName</span></span>
<span data-ttu-id="a0a2d-131">Specifica il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="a0a2d-132">Se questo parametro viene specificato, questo cmdlet trova un utente in base al nome.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="a0a2d-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a2d-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="a0a2d-134">-GroupId</span></span>
<span data-ttu-id="a0a2d-135">Specifica l'identificatore del gruppo.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-135">Specifies the group identifier.</span></span>
<span data-ttu-id="a0a2d-136">Se specificato, questo cmdlet trova tutti gli utenti all'interno del gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="a0a2d-137">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a2d-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="a0a2d-138">-LastName</span></span>
<span data-ttu-id="a0a2d-139">Specifica il cognome di un utente.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="a0a2d-140">Se specificato, questo cmdlet trova gli utenti in base al cognome.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="a0a2d-141">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-141">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a2d-142">-Stato</span><span class="sxs-lookup"><span data-stu-id="a0a2d-142">-State</span></span>
<span data-ttu-id="a0a2d-143">Specifica lo stato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-143">Specifies the user state.</span></span>
<span data-ttu-id="a0a2d-144">Se specificato, questo cmdlet trova gli utenti in questo stato.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="a0a2d-145">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-145">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: GetByUser
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a2d-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="a0a2d-146">-UserId</span></span>
<span data-ttu-id="a0a2d-147">Specifica un ID utente.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-147">Specifies a user ID.</span></span>
<span data-ttu-id="a0a2d-148">Se specificato, questo cmdlet trova l'utente tramite questo identificatore.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="a0a2d-149">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-149">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a2d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a2d-150">CommonParameters</span></span>
<span data-ttu-id="a0a2d-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0a2d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a2d-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0a2d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a2d-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0a2d-153">INPUTS</span></span>

### <span data-ttu-id="a0a2d-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a0a2d-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a0a2d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="a0a2d-155">System.String</span></span>

### <span data-ttu-id="a0a2d-156">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a0a2d-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a0a2d-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0a2d-157">OUTPUTS</span></span>

### <span data-ttu-id="a0a2d-158">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a0a2d-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="a0a2d-159">Note</span><span class="sxs-lookup"><span data-stu-id="a0a2d-159">NOTES</span></span>

## <span data-ttu-id="a0a2d-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0a2d-160">RELATED LINKS</span></span>

[<span data-ttu-id="a0a2d-161">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a0a2d-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="a0a2d-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a0a2d-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="a0a2d-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a0a2d-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


