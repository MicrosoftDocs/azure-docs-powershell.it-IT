---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 07f387239bdaad526c36c3928e7d2c5f490b0c7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514584"
---
# <span data-ttu-id="f5d21-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f5d21-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="f5d21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f5d21-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d21-103">Ottiene un utente o utenti.</span><span class="sxs-lookup"><span data-stu-id="f5d21-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5d21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5d21-104">SYNTAX</span></span>

### <span data-ttu-id="f5d21-105">GeAllUsers (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f5d21-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5d21-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="f5d21-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5d21-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="f5d21-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5d21-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5d21-108">DESCRIPTION</span></span>
<span data-ttu-id="f5d21-109">Il cmdlet **Get-AzureRmApiManagementUser** ottiene un utente specificato o tutti gli utenti, se non è specificato alcun utente.</span><span class="sxs-lookup"><span data-stu-id="f5d21-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="f5d21-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5d21-110">EXAMPLES</span></span>

### <span data-ttu-id="f5d21-111">Esempio 1: ottenere tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="f5d21-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="f5d21-112">Questo comando consente di ottenere tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="f5d21-112">This command gets all users.</span></span>

### <span data-ttu-id="f5d21-113">Esempio 2: ottenere un utente tramite ID</span><span class="sxs-lookup"><span data-stu-id="f5d21-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="f5d21-114">Questo comando consente di ottenere un utente in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="f5d21-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="f5d21-115">Esempio: ottenere gli utenti per Cognome</span><span class="sxs-lookup"><span data-stu-id="f5d21-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="f5d21-116">Questo comando ottiene gli utenti con un cognome specificato, Fuller.</span><span class="sxs-lookup"><span data-stu-id="f5d21-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="f5d21-117">Esempio 4: ottenere un utente tramite indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="f5d21-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="f5d21-118">Questo comando consente di ottenere l'utente con l'indirizzo di posta elettronica specificato.</span><span class="sxs-lookup"><span data-stu-id="f5d21-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="f5d21-119">Esempio 5: ottenere tutti gli utenti all'interno di un gruppo</span><span class="sxs-lookup"><span data-stu-id="f5d21-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="f5d21-120">Questo comando consente di ottenere tutti gli utenti all'interno del gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="f5d21-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="f5d21-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f5d21-121">PARAMETERS</span></span>

### <span data-ttu-id="f5d21-122">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f5d21-122">-Context</span></span>
<span data-ttu-id="f5d21-123">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5d21-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d21-124">-DefaultProfile</span></span>
<span data-ttu-id="f5d21-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5d21-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d21-126">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="f5d21-126">-Email</span></span>
<span data-ttu-id="f5d21-127">Specifica l'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f5d21-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="f5d21-128">Se questo parametro viene specificato, questo cmdlet trova un utente tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="f5d21-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="f5d21-129">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f5d21-129">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5d21-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="f5d21-130">-FirstName</span></span>
<span data-ttu-id="f5d21-131">Specifica il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f5d21-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="f5d21-132">Se questo parametro viene specificato, questo cmdlet trova un utente in base al nome.</span><span class="sxs-lookup"><span data-stu-id="f5d21-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="f5d21-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f5d21-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5d21-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f5d21-134">-GroupId</span></span>
<span data-ttu-id="f5d21-135">Specifica l'identificatore del gruppo.</span><span class="sxs-lookup"><span data-stu-id="f5d21-135">Specifies the group identifier.</span></span>
<span data-ttu-id="f5d21-136">Se specificato, questo cmdlet trova tutti gli utenti all'interno del gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="f5d21-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="f5d21-137">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f5d21-137">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5d21-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="f5d21-138">-LastName</span></span>
<span data-ttu-id="f5d21-139">Specifica il cognome di un utente.</span><span class="sxs-lookup"><span data-stu-id="f5d21-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="f5d21-140">Se specificato, questo cmdlet trova gli utenti in base al cognome.</span><span class="sxs-lookup"><span data-stu-id="f5d21-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="f5d21-141">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f5d21-141">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5d21-142">-Stato</span><span class="sxs-lookup"><span data-stu-id="f5d21-142">-State</span></span>
<span data-ttu-id="f5d21-143">Specifica lo stato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f5d21-143">Specifies the user state.</span></span>
<span data-ttu-id="f5d21-144">Se specificato, questo cmdlet trova gli utenti in questo stato.</span><span class="sxs-lookup"><span data-stu-id="f5d21-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="f5d21-145">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f5d21-145">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: GetByUser
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5d21-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="f5d21-146">-UserId</span></span>
<span data-ttu-id="f5d21-147">Specifica un ID utente.</span><span class="sxs-lookup"><span data-stu-id="f5d21-147">Specifies a user ID.</span></span>
<span data-ttu-id="f5d21-148">Se specificato, questo cmdlet trova l'utente tramite questo identificatore.</span><span class="sxs-lookup"><span data-stu-id="f5d21-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="f5d21-149">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f5d21-149">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5d21-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d21-150">CommonParameters</span></span>
<span data-ttu-id="f5d21-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5d21-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d21-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5d21-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d21-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f5d21-153">INPUTS</span></span>

### <span data-ttu-id="f5d21-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f5d21-154">None</span></span>
<span data-ttu-id="f5d21-155">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f5d21-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5d21-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5d21-156">OUTPUTS</span></span>

### <span data-ttu-id="f5d21-157">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f5d21-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>
<span data-ttu-id="f5d21-158">Dettagli dell'utente nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="f5d21-158">The details of User in API Management service.</span></span>

### <span data-ttu-id="f5d21-159">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser></span><span class="sxs-lookup"><span data-stu-id="f5d21-159">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>
<span data-ttu-id="f5d21-160">L'elenco di utenti nel servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="f5d21-160">The list of User in the API Management  service.</span></span>

## <span data-ttu-id="f5d21-161">Note</span><span class="sxs-lookup"><span data-stu-id="f5d21-161">NOTES</span></span>

## <span data-ttu-id="f5d21-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5d21-162">RELATED LINKS</span></span>

[<span data-ttu-id="f5d21-163">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f5d21-163">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="f5d21-164">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f5d21-164">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="f5d21-165">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f5d21-165">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


