---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488636"
---
# <span data-ttu-id="58e15-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="58e15-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="58e15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58e15-102">SYNOPSIS</span></span>
<span data-ttu-id="58e15-103">Carica il contenuto in un endpoint.</span><span class="sxs-lookup"><span data-stu-id="58e15-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="58e15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58e15-104">SYNTAX</span></span>

### <span data-ttu-id="58e15-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58e15-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58e15-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58e15-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58e15-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58e15-107">DESCRIPTION</span></span>
<span data-ttu-id="58e15-108">Il cmdlet **Publish-AzCdnEndpointContent** carica il contenuto da un server di origine per l'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="58e15-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="58e15-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58e15-109">EXAMPLES</span></span>

## <span data-ttu-id="58e15-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58e15-110">PARAMETERS</span></span>

### <span data-ttu-id="58e15-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="58e15-111">-CdnEndpoint</span></span>
<span data-ttu-id="58e15-112">Specifica l'endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="58e15-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="58e15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e15-113">-DefaultProfile</span></span>
<span data-ttu-id="58e15-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="58e15-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58e15-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="58e15-115">-EndpointName</span></span>
<span data-ttu-id="58e15-116">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="58e15-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="58e15-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="58e15-117">-LoadContent</span></span>
<span data-ttu-id="58e15-118">Specifica una matrice di percorsi relativi per il contenuto nel server di origine che questo cmdlet pubblica.</span><span class="sxs-lookup"><span data-stu-id="58e15-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="58e15-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58e15-119">-PassThru</span></span>
<span data-ttu-id="58e15-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="58e15-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="58e15-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="58e15-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58e15-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="58e15-122">-ProfileName</span></span>
<span data-ttu-id="58e15-123">Specifica il nome del profilo a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="58e15-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="58e15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e15-124">-ResourceGroupName</span></span>
<span data-ttu-id="58e15-125">Specifica il nome del gruppo di risorse a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="58e15-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="58e15-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e15-126">CommonParameters</span></span>
<span data-ttu-id="58e15-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e15-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e15-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58e15-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e15-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58e15-129">INPUTS</span></span>

### <span data-ttu-id="58e15-130">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="58e15-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="58e15-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="58e15-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="58e15-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58e15-132">OUTPUTS</span></span>

### <span data-ttu-id="58e15-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58e15-133">System.Boolean</span></span>

## <span data-ttu-id="58e15-134">Note</span><span class="sxs-lookup"><span data-stu-id="58e15-134">NOTES</span></span>

## <span data-ttu-id="58e15-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58e15-135">RELATED LINKS</span></span>

[<span data-ttu-id="58e15-136">Annulla pubblicazione-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="58e15-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


