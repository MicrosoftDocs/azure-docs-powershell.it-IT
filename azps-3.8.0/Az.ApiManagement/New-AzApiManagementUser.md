---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 6cc922ceb09509e70a4017241dc6beb6e5443d1a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020165"
---
# <span data-ttu-id="da93c-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="da93c-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="da93c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da93c-102">SYNOPSIS</span></span>
<span data-ttu-id="da93c-103">Registra un nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="da93c-103">Registers a new user.</span></span>

## <span data-ttu-id="da93c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da93c-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da93c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da93c-105">DESCRIPTION</span></span>
<span data-ttu-id="da93c-106">Il cmdlet **New-AzApiManagementUser** registra un nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="da93c-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="da93c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da93c-107">EXAMPLES</span></span>

### <span data-ttu-id="da93c-108">Esempio 1: registrare un nuovo utente</span><span class="sxs-lookup"><span data-stu-id="da93c-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="da93c-109">Questo comando registra un nuovo utente di nome Patti Fuller.</span><span class="sxs-lookup"><span data-stu-id="da93c-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="da93c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da93c-110">PARAMETERS</span></span>

### <span data-ttu-id="da93c-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="da93c-111">-Context</span></span>
<span data-ttu-id="da93c-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="da93c-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="da93c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da93c-113">-DefaultProfile</span></span>
<span data-ttu-id="da93c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da93c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da93c-115">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="da93c-115">-Email</span></span>
<span data-ttu-id="da93c-116">Specifica l'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="da93c-116">Specifies the email address of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da93c-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="da93c-117">-FirstName</span></span>
<span data-ttu-id="da93c-118">Specifica il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="da93c-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="da93c-119">Questo parametro deve essere lungo da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="da93c-119">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da93c-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="da93c-120">-LastName</span></span>
<span data-ttu-id="da93c-121">Specifica il cognome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="da93c-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="da93c-122">Questo parametro deve essere lungo da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="da93c-122">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da93c-123">-Nota</span><span class="sxs-lookup"><span data-stu-id="da93c-123">-Note</span></span>
<span data-ttu-id="da93c-124">Specifica una nota relativa all'utente.</span><span class="sxs-lookup"><span data-stu-id="da93c-124">Specifies a note about the user.</span></span>
<span data-ttu-id="da93c-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da93c-125">This parameter is optional.</span></span>
<span data-ttu-id="da93c-126">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="da93c-126">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da93c-127">-Password</span><span class="sxs-lookup"><span data-stu-id="da93c-127">-Password</span></span>
<span data-ttu-id="da93c-128">Specifica la password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="da93c-128">Specifies the user password.</span></span>
<span data-ttu-id="da93c-129">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="da93c-129">This parameter is required.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da93c-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="da93c-130">-State</span></span>
<span data-ttu-id="da93c-131">Specifica lo stato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="da93c-131">Specifies the user state.</span></span>
<span data-ttu-id="da93c-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da93c-132">This parameter is optional.</span></span>
<span data-ttu-id="da93c-133">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="da93c-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da93c-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="da93c-134">-UserId</span></span>
<span data-ttu-id="da93c-135">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="da93c-135">Specifies the user ID.</span></span>
<span data-ttu-id="da93c-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da93c-136">This parameter is optional.</span></span>
<span data-ttu-id="da93c-137">Se questo parametro non viene specificato, questo cmdlet genera un ID utente.</span><span class="sxs-lookup"><span data-stu-id="da93c-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da93c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da93c-138">CommonParameters</span></span>
<span data-ttu-id="da93c-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da93c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da93c-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da93c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da93c-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da93c-141">INPUTS</span></span>

### <span data-ttu-id="da93c-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="da93c-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="da93c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="da93c-143">System.String</span></span>

### <span data-ttu-id="da93c-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="da93c-144">System.Security.SecureString</span></span>

### <span data-ttu-id="da93c-145">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="da93c-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="da93c-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da93c-146">OUTPUTS</span></span>

### <span data-ttu-id="da93c-147">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="da93c-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="da93c-148">Note</span><span class="sxs-lookup"><span data-stu-id="da93c-148">NOTES</span></span>

## <span data-ttu-id="da93c-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da93c-149">RELATED LINKS</span></span>

[<span data-ttu-id="da93c-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="da93c-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="da93c-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="da93c-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


