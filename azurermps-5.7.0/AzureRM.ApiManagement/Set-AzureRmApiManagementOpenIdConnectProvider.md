---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c914c49aeb4f2a763a09c5b513bcbe7809110b05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521467"
---
# <span data-ttu-id="3d9c5-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3d9c5-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="3d9c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d9c5-102">SYNOPSIS</span></span>
<span data-ttu-id="3d9c5-103">Modifica un provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d9c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d9c5-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d9c5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d9c5-105">DESCRIPTION</span></span>
<span data-ttu-id="3d9c5-106">Il cmdlet **set-AzureRmApiManagementOpenIdConnectProvider** modifica un provider di connessione OpenID in gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="3d9c5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d9c5-107">EXAMPLES</span></span>

### <span data-ttu-id="3d9c5-108">Esempio 1: cambiare il segreto del client per un provider</span><span class="sxs-lookup"><span data-stu-id="3d9c5-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="3d9c5-109">Questo comando modifica il provider con ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="3d9c5-110">Il comando specifica un segreto client per il provider.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="3d9c5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d9c5-111">PARAMETERS</span></span>

### <span data-ttu-id="3d9c5-112">-ClientID</span><span class="sxs-lookup"><span data-stu-id="3d9c5-112">-ClientId</span></span>
<span data-ttu-id="3d9c5-113">Specifica l'ID client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="3d9c5-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="3d9c5-114">-ClientSecret</span></span>
<span data-ttu-id="3d9c5-115">Specifica il segreto client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="3d9c5-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3d9c5-116">-Context</span></span>
<span data-ttu-id="3d9c5-117">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3d9c5-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3d9c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d9c5-118">-DefaultProfile</span></span>
<span data-ttu-id="3d9c5-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3d9c5-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d9c5-120">-Description</span></span>
<span data-ttu-id="3d9c5-121">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-121">Specifies a description.</span></span>

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

### <span data-ttu-id="3d9c5-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="3d9c5-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="3d9c5-123">Specifica un URI di endpoint dei metadati del provider.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="3d9c5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d9c5-124">-Name</span></span>
<span data-ttu-id="3d9c5-125">Specifica un nome descrittivo per il provider.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="3d9c5-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="3d9c5-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="3d9c5-127">Specifica un ID per il provider modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="3d9c5-128">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="3d9c5-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d9c5-129">-PassThru</span></span>
<span data-ttu-id="3d9c5-130">Indica che questo cmdlet restituisce il **PsApiManagementOpenIdConnectProvider** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d9c5-131">CommonParameters</span></span>
<span data-ttu-id="3d9c5-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d9c5-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d9c5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d9c5-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d9c5-134">INPUTS</span></span>

### <span data-ttu-id="3d9c5-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3d9c5-135">None</span></span>
<span data-ttu-id="3d9c5-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3d9c5-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d9c5-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d9c5-137">OUTPUTS</span></span>

### <span data-ttu-id="3d9c5-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3d9c5-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="3d9c5-139">Note</span><span class="sxs-lookup"><span data-stu-id="3d9c5-139">NOTES</span></span>

## <span data-ttu-id="3d9c5-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d9c5-140">RELATED LINKS</span></span>

[<span data-ttu-id="3d9c5-141">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3d9c5-141">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="3d9c5-142">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3d9c5-142">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="3d9c5-143">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3d9c5-143">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


