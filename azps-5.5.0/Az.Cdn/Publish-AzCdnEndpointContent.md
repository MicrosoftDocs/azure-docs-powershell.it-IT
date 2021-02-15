---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200774"
---
# <span data-ttu-id="fa47f-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="fa47f-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="fa47f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa47f-102">SYNOPSIS</span></span>
<span data-ttu-id="fa47f-103">Carica il contenuto in un endpoint.</span><span class="sxs-lookup"><span data-stu-id="fa47f-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="fa47f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa47f-104">SYNTAX</span></span>

### <span data-ttu-id="fa47f-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa47f-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa47f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa47f-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa47f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fa47f-107">DESCRIPTION</span></span>
<span data-ttu-id="fa47f-108">Il cmdlet **Publish-AzCdnEndpointContent** carica il contenuto da un server di origine per l'endpoint rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="fa47f-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="fa47f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa47f-109">EXAMPLES</span></span>

## <span data-ttu-id="fa47f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa47f-110">PARAMETERS</span></span>

### <span data-ttu-id="fa47f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa47f-111">-CdnEndpoint</span></span>
<span data-ttu-id="fa47f-112">Specifica l'endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="fa47f-112">Specifies the CDN endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa47f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa47f-113">-DefaultProfile</span></span>
<span data-ttu-id="fa47f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="fa47f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa47f-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fa47f-115">-EndpointName</span></span>
<span data-ttu-id="fa47f-116">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="fa47f-116">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa47f-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="fa47f-117">-LoadContent</span></span>
<span data-ttu-id="fa47f-118">Specifica una matrice di percorsi relativi per il contenuto nel server di origine pubblicato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa47f-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa47f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa47f-119">-PassThru</span></span>
<span data-ttu-id="fa47f-120">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="fa47f-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fa47f-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="fa47f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fa47f-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fa47f-122">-ProfileName</span></span>
<span data-ttu-id="fa47f-123">Specifica il nome del profilo a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="fa47f-123">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa47f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa47f-124">-ResourceGroupName</span></span>
<span data-ttu-id="fa47f-125">Specifica il nome del gruppo di risorse a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="fa47f-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa47f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa47f-126">CommonParameters</span></span>
<span data-ttu-id="fa47f-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa47f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa47f-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fa47f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa47f-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="fa47f-129">INPUTS</span></span>

### <span data-ttu-id="fa47f-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa47f-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="fa47f-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa47f-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fa47f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa47f-132">OUTPUTS</span></span>

### <span data-ttu-id="fa47f-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa47f-133">System.Boolean</span></span>

## <span data-ttu-id="fa47f-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="fa47f-134">NOTES</span></span>

## <span data-ttu-id="fa47f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa47f-135">RELATED LINKS</span></span>

[<span data-ttu-id="fa47f-136">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="fa47f-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


