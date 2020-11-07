---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: fa7b44710aa51a138729d9a04a41a82ec2769f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688591"
---
# <span data-ttu-id="60d65-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="60d65-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="60d65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60d65-102">SYNOPSIS</span></span>
<span data-ttu-id="60d65-103">Registra un nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="60d65-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60d65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60d65-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60d65-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60d65-105">DESCRIPTION</span></span>
<span data-ttu-id="60d65-106">Il cmdlet **New-AzureRmApiManagementUser** registra un nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="60d65-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="60d65-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60d65-107">EXAMPLES</span></span>

### <span data-ttu-id="60d65-108">Esempio 1: registrare un nuovo utente</span><span class="sxs-lookup"><span data-stu-id="60d65-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="60d65-109">Questo comando registra un nuovo utente di nome Patti Fuller.</span><span class="sxs-lookup"><span data-stu-id="60d65-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="60d65-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60d65-110">PARAMETERS</span></span>

### <span data-ttu-id="60d65-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="60d65-111">-Context</span></span>
<span data-ttu-id="60d65-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="60d65-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="60d65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d65-113">-DefaultProfile</span></span>
<span data-ttu-id="60d65-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60d65-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="60d65-115">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="60d65-115">-Email</span></span>
<span data-ttu-id="60d65-116">Specifica l'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="60d65-116">Specifies the email address of the user.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60d65-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="60d65-117">-FirstName</span></span>
<span data-ttu-id="60d65-118">Specifica il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="60d65-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="60d65-119">Questo parametro deve essere lungo da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="60d65-119">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60d65-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="60d65-120">-LastName</span></span>
<span data-ttu-id="60d65-121">Specifica il cognome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="60d65-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="60d65-122">Questo parametro deve essere lungo da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="60d65-122">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60d65-123">-Nota</span><span class="sxs-lookup"><span data-stu-id="60d65-123">-Note</span></span>
<span data-ttu-id="60d65-124">Specifica una nota relativa all'utente.</span><span class="sxs-lookup"><span data-stu-id="60d65-124">Specifies a note about the user.</span></span>
<span data-ttu-id="60d65-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="60d65-125">This parameter is optional.</span></span>
<span data-ttu-id="60d65-126">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="60d65-126">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60d65-127">-Password</span><span class="sxs-lookup"><span data-stu-id="60d65-127">-Password</span></span>
<span data-ttu-id="60d65-128">Specifica la password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="60d65-128">Specifies the user password.</span></span>
<span data-ttu-id="60d65-129">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="60d65-129">This parameter is required.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60d65-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="60d65-130">-State</span></span>
<span data-ttu-id="60d65-131">Specifica lo stato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="60d65-131">Specifies the user state.</span></span>
<span data-ttu-id="60d65-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="60d65-132">This parameter is optional.</span></span>
<span data-ttu-id="60d65-133">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="60d65-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60d65-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="60d65-134">-UserId</span></span>
<span data-ttu-id="60d65-135">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="60d65-135">Specifies the user ID.</span></span>
<span data-ttu-id="60d65-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="60d65-136">This parameter is optional.</span></span>
<span data-ttu-id="60d65-137">Se questo parametro non viene specificato, questo cmdlet genera un ID utente.</span><span class="sxs-lookup"><span data-stu-id="60d65-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60d65-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d65-138">CommonParameters</span></span>
<span data-ttu-id="60d65-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60d65-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d65-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60d65-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d65-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60d65-141">INPUTS</span></span>

### <span data-ttu-id="60d65-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="60d65-142">None</span></span>
<span data-ttu-id="60d65-143">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="60d65-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60d65-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60d65-144">OUTPUTS</span></span>

### <span data-ttu-id="60d65-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="60d65-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="60d65-146">Note</span><span class="sxs-lookup"><span data-stu-id="60d65-146">NOTES</span></span>

## <span data-ttu-id="60d65-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60d65-147">RELATED LINKS</span></span>

[<span data-ttu-id="60d65-148">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="60d65-148">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="60d65-149">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="60d65-149">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


