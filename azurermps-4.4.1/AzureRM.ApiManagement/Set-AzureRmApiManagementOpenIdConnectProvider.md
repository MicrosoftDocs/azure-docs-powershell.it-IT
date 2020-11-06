---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f890236907ea0a717245d9345be276a6ccf04b8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518416"
---
# <span data-ttu-id="c136a-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c136a-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="c136a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c136a-102">SYNOPSIS</span></span>
<span data-ttu-id="c136a-103">Modifica un provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="c136a-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c136a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c136a-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c136a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c136a-105">DESCRIPTION</span></span>
<span data-ttu-id="c136a-106">Il cmdlet **set-AzureRmApiManagementOpenIdConnectProvider** modifica un provider di connessione OpenID in gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="c136a-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="c136a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c136a-107">EXAMPLES</span></span>

### <span data-ttu-id="c136a-108">Esempio 1: cambiare il segreto del client per un provider</span><span class="sxs-lookup"><span data-stu-id="c136a-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="c136a-109">Questo comando modifica il provider con ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="c136a-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="c136a-110">Il comando specifica un segreto client per il provider.</span><span class="sxs-lookup"><span data-stu-id="c136a-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="c136a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c136a-111">PARAMETERS</span></span>

### <span data-ttu-id="c136a-112">-ClientID</span><span class="sxs-lookup"><span data-stu-id="c136a-112">-ClientId</span></span>
<span data-ttu-id="c136a-113">Specifica l'ID client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="c136a-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="c136a-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="c136a-114">-ClientSecret</span></span>
<span data-ttu-id="c136a-115">Specifica il segreto client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="c136a-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="c136a-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c136a-116">-Context</span></span>
<span data-ttu-id="c136a-117">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c136a-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c136a-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c136a-118">-Description</span></span>
<span data-ttu-id="c136a-119">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="c136a-119">Specifies a description.</span></span>

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

### <span data-ttu-id="c136a-120">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="c136a-120">-MetadataEndpointUri</span></span>
<span data-ttu-id="c136a-121">Specifica un URI di endpoint dei metadati del provider.</span><span class="sxs-lookup"><span data-stu-id="c136a-121">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="c136a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c136a-122">-Name</span></span>
<span data-ttu-id="c136a-123">Specifica un nome descrittivo per il provider.</span><span class="sxs-lookup"><span data-stu-id="c136a-123">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="c136a-124">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="c136a-124">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="c136a-125">Specifica un ID per il provider modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c136a-125">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="c136a-126">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="c136a-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="c136a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c136a-127">-PassThru</span></span>
<span data-ttu-id="c136a-128">Indica che questo cmdlet restituisce il **PsApiManagementOpenIdConnectProvider** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c136a-128">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c136a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c136a-129">-DefaultProfile</span></span>
<span data-ttu-id="c136a-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c136a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c136a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c136a-131">CommonParameters</span></span>
<span data-ttu-id="c136a-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c136a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c136a-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c136a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c136a-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c136a-134">INPUTS</span></span>

## <span data-ttu-id="c136a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c136a-135">OUTPUTS</span></span>

### <span data-ttu-id="c136a-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c136a-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="c136a-137">Note</span><span class="sxs-lookup"><span data-stu-id="c136a-137">NOTES</span></span>

## <span data-ttu-id="c136a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c136a-138">RELATED LINKS</span></span>

[<span data-ttu-id="c136a-139">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c136a-139">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="c136a-140">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c136a-140">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="c136a-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c136a-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


