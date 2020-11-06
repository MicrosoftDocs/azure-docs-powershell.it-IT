---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508835"
---
# <span data-ttu-id="fc07c-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fc07c-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="fc07c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc07c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc07c-103">Ottiene un utente o utenti.</span><span class="sxs-lookup"><span data-stu-id="fc07c-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc07c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc07c-104">SYNTAX</span></span>

### <span data-ttu-id="fc07c-105">Ottenere tutti gli utenti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fc07c-105">Get all users (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc07c-106">Ottenere l'utente per ID</span><span class="sxs-lookup"><span data-stu-id="fc07c-106">Get user by ID</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc07c-107">Trovare utenti</span><span class="sxs-lookup"><span data-stu-id="fc07c-107">Find users</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc07c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc07c-108">DESCRIPTION</span></span>
<span data-ttu-id="fc07c-109">Il cmdlet **Get-AzureRmApiManagementUser** ottiene un utente specificato o tutti gli utenti, se non è specificato alcun utente.</span><span class="sxs-lookup"><span data-stu-id="fc07c-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="fc07c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc07c-110">EXAMPLES</span></span>

### <span data-ttu-id="fc07c-111">Esempio 1: ottenere tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="fc07c-111">Example 1: Get all users</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="fc07c-112">Questo comando consente di ottenere tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="fc07c-112">This command gets all users.</span></span>

### <span data-ttu-id="fc07c-113">Esempio 2: ottenere un utente tramite ID</span><span class="sxs-lookup"><span data-stu-id="fc07c-113">Example 2: Get a user by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="fc07c-114">Questo comando consente di ottenere un utente in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="fc07c-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="fc07c-115">Esempio: ottenere gli utenti per Cognome</span><span class="sxs-lookup"><span data-stu-id="fc07c-115">Example: Get users by last name</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="fc07c-116">Questo comando ottiene gli utenti con un cognome specificato, Fuller.</span><span class="sxs-lookup"><span data-stu-id="fc07c-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="fc07c-117">Esempio 4: ottenere un utente tramite indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="fc07c-117">Example 4: Get a user by email address</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

<span data-ttu-id="fc07c-118">Questo comando consente di ottenere l'utente con l'indirizzo di posta elettronica specificato.</span><span class="sxs-lookup"><span data-stu-id="fc07c-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="fc07c-119">Esempio 5: ottenere tutti gli utenti all'interno di un gruppo</span><span class="sxs-lookup"><span data-stu-id="fc07c-119">Example 5: Get all users within a group</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="fc07c-120">Questo comando consente di ottenere tutti gli utenti all'interno del gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="fc07c-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="fc07c-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc07c-121">PARAMETERS</span></span>

### <span data-ttu-id="fc07c-122">-Contesto</span><span class="sxs-lookup"><span data-stu-id="fc07c-122">-Context</span></span>
<span data-ttu-id="fc07c-123">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="fc07c-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="fc07c-124">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="fc07c-124">-Email</span></span>
<span data-ttu-id="fc07c-125">Specifica l'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fc07c-125">Specifies the email address of the user.</span></span>
<span data-ttu-id="fc07c-126">Se questo parametro viene specificato, questo cmdlet trova un utente tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="fc07c-126">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="fc07c-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc07c-127">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc07c-128">-FirstName</span><span class="sxs-lookup"><span data-stu-id="fc07c-128">-FirstName</span></span>
<span data-ttu-id="fc07c-129">Specifica il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fc07c-129">Specifies the first name of the user.</span></span>
<span data-ttu-id="fc07c-130">Se questo parametro viene specificato, questo cmdlet trova un utente in base al nome.</span><span class="sxs-lookup"><span data-stu-id="fc07c-130">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="fc07c-131">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc07c-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc07c-132">-GroupId</span><span class="sxs-lookup"><span data-stu-id="fc07c-132">-GroupId</span></span>
<span data-ttu-id="fc07c-133">Specifica l'identificatore del gruppo.</span><span class="sxs-lookup"><span data-stu-id="fc07c-133">Specifies the group identifier.</span></span>
<span data-ttu-id="fc07c-134">Se specificato, questo cmdlet trova tutti gli utenti all'interno del gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="fc07c-134">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="fc07c-135">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc07c-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc07c-136">-LastName</span><span class="sxs-lookup"><span data-stu-id="fc07c-136">-LastName</span></span>
<span data-ttu-id="fc07c-137">Specifica il cognome di un utente.</span><span class="sxs-lookup"><span data-stu-id="fc07c-137">Specifies the last name of a user.</span></span>
<span data-ttu-id="fc07c-138">Se specificato, questo cmdlet trova gli utenti in base al cognome.</span><span class="sxs-lookup"><span data-stu-id="fc07c-138">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="fc07c-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc07c-139">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc07c-140">-Stato</span><span class="sxs-lookup"><span data-stu-id="fc07c-140">-State</span></span>
<span data-ttu-id="fc07c-141">Specifica lo stato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fc07c-141">Specifies the user state.</span></span>
<span data-ttu-id="fc07c-142">Se specificato, questo cmdlet trova gli utenti in questo stato.</span><span class="sxs-lookup"><span data-stu-id="fc07c-142">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="fc07c-143">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc07c-143">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc07c-144">-UserId</span><span class="sxs-lookup"><span data-stu-id="fc07c-144">-UserId</span></span>
<span data-ttu-id="fc07c-145">Specifica un ID utente.</span><span class="sxs-lookup"><span data-stu-id="fc07c-145">Specifies a user ID.</span></span>
<span data-ttu-id="fc07c-146">Se specificato, questo cmdlet trova l'utente tramite questo identificatore.</span><span class="sxs-lookup"><span data-stu-id="fc07c-146">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="fc07c-147">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc07c-147">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc07c-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc07c-148">-DefaultProfile</span></span>
<span data-ttu-id="fc07c-149">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc07c-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc07c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc07c-150">CommonParameters</span></span>
<span data-ttu-id="fc07c-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc07c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc07c-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc07c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc07c-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc07c-153">INPUTS</span></span>

## <span data-ttu-id="fc07c-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc07c-154">OUTPUTS</span></span>

### <span data-ttu-id="fc07c-155">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser></span><span class="sxs-lookup"><span data-stu-id="fc07c-155">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>

## <span data-ttu-id="fc07c-156">Note</span><span class="sxs-lookup"><span data-stu-id="fc07c-156">NOTES</span></span>

## <span data-ttu-id="fc07c-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc07c-157">RELATED LINKS</span></span>

[<span data-ttu-id="fc07c-158">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fc07c-158">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="fc07c-159">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fc07c-159">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="fc07c-160">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fc07c-160">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


