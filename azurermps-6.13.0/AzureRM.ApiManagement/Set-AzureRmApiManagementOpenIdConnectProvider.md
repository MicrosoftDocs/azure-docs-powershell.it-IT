---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6f568f27cf5b50cd517d8133578d6cf36060252f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509435"
---
# <span data-ttu-id="b1cf3-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b1cf3-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b1cf3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="b1cf3-103">Modifica un provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1cf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1cf3-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1cf3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1cf3-105">DESCRIPTION</span></span>
<span data-ttu-id="b1cf3-106">Il cmdlet **set-AzureRmApiManagementOpenIdConnectProvider** modifica un provider di connessione OpenID in gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="b1cf3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1cf3-107">EXAMPLES</span></span>

### <span data-ttu-id="b1cf3-108">Esempio 1: cambiare il segreto del client per un provider</span><span class="sxs-lookup"><span data-stu-id="b1cf3-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="b1cf3-109">Questo comando modifica il provider con ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="b1cf3-110">Il comando specifica un segreto client per il provider.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="b1cf3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1cf3-111">PARAMETERS</span></span>

### <span data-ttu-id="b1cf3-112">-ClientID</span><span class="sxs-lookup"><span data-stu-id="b1cf3-112">-ClientId</span></span>
<span data-ttu-id="b1cf3-113">Specifica l'ID client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="b1cf3-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="b1cf3-114">-ClientSecret</span></span>
<span data-ttu-id="b1cf3-115">Specifica il segreto client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="b1cf3-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b1cf3-116">-Context</span></span>
<span data-ttu-id="b1cf3-117">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b1cf3-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b1cf3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1cf3-118">-DefaultProfile</span></span>
<span data-ttu-id="b1cf3-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1cf3-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1cf3-120">-Description</span></span>
<span data-ttu-id="b1cf3-121">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-121">Specifies a description.</span></span>

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

### <span data-ttu-id="b1cf3-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="b1cf3-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="b1cf3-123">Specifica un URI di endpoint dei metadati del provider.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="b1cf3-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1cf3-124">-Name</span></span>
<span data-ttu-id="b1cf3-125">Specifica un nome descrittivo per il provider.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="b1cf3-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b1cf3-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="b1cf3-127">Specifica un ID per il provider modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="b1cf3-128">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="b1cf3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1cf3-129">-PassThru</span></span>
<span data-ttu-id="b1cf3-130">Indica che questo cmdlet restituisce il **PsApiManagementOpenIdConnectProvider** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1cf3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1cf3-131">CommonParameters</span></span>
<span data-ttu-id="b1cf3-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1cf3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1cf3-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1cf3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1cf3-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1cf3-134">INPUTS</span></span>

### <span data-ttu-id="b1cf3-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b1cf3-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b1cf3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b1cf3-136">System.String</span></span>

### <span data-ttu-id="b1cf3-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b1cf3-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b1cf3-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1cf3-138">OUTPUTS</span></span>

### <span data-ttu-id="b1cf3-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b1cf3-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b1cf3-140">Note</span><span class="sxs-lookup"><span data-stu-id="b1cf3-140">NOTES</span></span>

## <span data-ttu-id="b1cf3-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1cf3-141">RELATED LINKS</span></span>

[<span data-ttu-id="b1cf3-142">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b1cf3-142">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b1cf3-143">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b1cf3-143">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b1cf3-144">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b1cf3-144">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


