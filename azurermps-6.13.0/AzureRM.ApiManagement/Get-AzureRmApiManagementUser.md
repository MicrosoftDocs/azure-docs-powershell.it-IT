---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 8f02b88115ec6dc415ecf6cf5464503d61778cca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517699"
---
# <span data-ttu-id="c670c-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c670c-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="c670c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c670c-102">SYNOPSIS</span></span>
<span data-ttu-id="c670c-103">Ottiene un utente o utenti.</span><span class="sxs-lookup"><span data-stu-id="c670c-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c670c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c670c-104">SYNTAX</span></span>

### <span data-ttu-id="c670c-105">GeAllUsers (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c670c-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c670c-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="c670c-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c670c-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="c670c-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c670c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c670c-108">DESCRIPTION</span></span>
<span data-ttu-id="c670c-109">Il cmdlet **Get-AzureRmApiManagementUser** ottiene un utente specificato o tutti gli utenti, se non è specificato alcun utente.</span><span class="sxs-lookup"><span data-stu-id="c670c-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="c670c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c670c-110">EXAMPLES</span></span>

### <span data-ttu-id="c670c-111">Esempio 1: ottenere tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="c670c-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="c670c-112">Questo comando consente di ottenere tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="c670c-112">This command gets all users.</span></span>

### <span data-ttu-id="c670c-113">Esempio 2: ottenere un utente tramite ID</span><span class="sxs-lookup"><span data-stu-id="c670c-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="c670c-114">Questo comando consente di ottenere un utente in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="c670c-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="c670c-115">Esempio: ottenere gli utenti per Cognome</span><span class="sxs-lookup"><span data-stu-id="c670c-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="c670c-116">Questo comando ottiene gli utenti con un cognome specificato, Fuller.</span><span class="sxs-lookup"><span data-stu-id="c670c-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="c670c-117">Esempio 4: ottenere un utente tramite indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="c670c-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="c670c-118">Questo comando consente di ottenere l'utente con l'indirizzo di posta elettronica specificato.</span><span class="sxs-lookup"><span data-stu-id="c670c-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="c670c-119">Esempio 5: ottenere tutti gli utenti all'interno di un gruppo</span><span class="sxs-lookup"><span data-stu-id="c670c-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="c670c-120">Questo comando consente di ottenere tutti gli utenti all'interno del gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="c670c-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="c670c-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c670c-121">PARAMETERS</span></span>

### <span data-ttu-id="c670c-122">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c670c-122">-Context</span></span>
<span data-ttu-id="c670c-123">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="c670c-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c670c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c670c-124">-DefaultProfile</span></span>
<span data-ttu-id="c670c-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c670c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c670c-126">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="c670c-126">-Email</span></span>
<span data-ttu-id="c670c-127">Specifica l'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c670c-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="c670c-128">Se questo parametro viene specificato, questo cmdlet trova un utente tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="c670c-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="c670c-129">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c670c-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="c670c-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="c670c-130">-FirstName</span></span>
<span data-ttu-id="c670c-131">Specifica il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c670c-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="c670c-132">Se questo parametro viene specificato, questo cmdlet trova un utente in base al nome.</span><span class="sxs-lookup"><span data-stu-id="c670c-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="c670c-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c670c-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="c670c-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="c670c-134">-GroupId</span></span>
<span data-ttu-id="c670c-135">Specifica l'identificatore del gruppo.</span><span class="sxs-lookup"><span data-stu-id="c670c-135">Specifies the group identifier.</span></span>
<span data-ttu-id="c670c-136">Se specificato, questo cmdlet trova tutti gli utenti all'interno del gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="c670c-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="c670c-137">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c670c-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="c670c-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="c670c-138">-LastName</span></span>
<span data-ttu-id="c670c-139">Specifica il cognome di un utente.</span><span class="sxs-lookup"><span data-stu-id="c670c-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="c670c-140">Se specificato, questo cmdlet trova gli utenti in base al cognome.</span><span class="sxs-lookup"><span data-stu-id="c670c-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="c670c-141">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c670c-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="c670c-142">-Stato</span><span class="sxs-lookup"><span data-stu-id="c670c-142">-State</span></span>
<span data-ttu-id="c670c-143">Specifica lo stato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c670c-143">Specifies the user state.</span></span>
<span data-ttu-id="c670c-144">Se specificato, questo cmdlet trova gli utenti in questo stato.</span><span class="sxs-lookup"><span data-stu-id="c670c-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="c670c-145">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c670c-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="c670c-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="c670c-146">-UserId</span></span>
<span data-ttu-id="c670c-147">Specifica un ID utente.</span><span class="sxs-lookup"><span data-stu-id="c670c-147">Specifies a user ID.</span></span>
<span data-ttu-id="c670c-148">Se specificato, questo cmdlet trova l'utente tramite questo identificatore.</span><span class="sxs-lookup"><span data-stu-id="c670c-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="c670c-149">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c670c-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="c670c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c670c-150">CommonParameters</span></span>
<span data-ttu-id="c670c-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c670c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c670c-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c670c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c670c-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c670c-153">INPUTS</span></span>

### <span data-ttu-id="c670c-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c670c-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c670c-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c670c-155">System.String</span></span>

### <span data-ttu-id="c670c-156">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState, Microsoft. Azure. Commands. ApiManagement. ServiceManagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c670c-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c670c-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c670c-157">OUTPUTS</span></span>

### <span data-ttu-id="c670c-158">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c670c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="c670c-159">Note</span><span class="sxs-lookup"><span data-stu-id="c670c-159">NOTES</span></span>

## <span data-ttu-id="c670c-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c670c-160">RELATED LINKS</span></span>

[<span data-ttu-id="c670c-161">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c670c-161">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="c670c-162">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c670c-162">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="c670c-163">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c670c-163">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


