---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: b4800b77441a82fc0e9966be16f91c9d81a2214a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685633"
---
# <span data-ttu-id="27e97-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="27e97-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="27e97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27e97-102">SYNOPSIS</span></span>
<span data-ttu-id="27e97-103">Ottiene un server di origine CDN.</span><span class="sxs-lookup"><span data-stu-id="27e97-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27e97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27e97-104">SYNTAX</span></span>

### <span data-ttu-id="27e97-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27e97-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27e97-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27e97-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27e97-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27e97-107">DESCRIPTION</span></span>
<span data-ttu-id="27e97-108">Il cmdlet **Get-AzureRmCdnOrigin** ottiene un server di origine della rete CDN (Azure Content Delivery Network) e i relativi dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="27e97-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="27e97-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27e97-109">EXAMPLES</span></span>

## <span data-ttu-id="27e97-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27e97-110">PARAMETERS</span></span>

### <span data-ttu-id="27e97-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="27e97-111">-CdnEndpoint</span></span>
<span data-ttu-id="27e97-112">Specifica l'oggetto endpoint CDN a cui appartiene l'origine.</span><span class="sxs-lookup"><span data-stu-id="27e97-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27e97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e97-113">-DefaultProfile</span></span>
<span data-ttu-id="27e97-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="27e97-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27e97-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="27e97-115">-EndpointName</span></span>
<span data-ttu-id="27e97-116">Specifica il nome dell'endpoint a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="27e97-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e97-117">-Originname</span><span class="sxs-lookup"><span data-stu-id="27e97-117">-OriginName</span></span>
<span data-ttu-id="27e97-118">Specifica il nome del server di origine.</span><span class="sxs-lookup"><span data-stu-id="27e97-118">Specifies the name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e97-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="27e97-119">-ProfileName</span></span>
<span data-ttu-id="27e97-120">Specifica il nome del profilo a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="27e97-120">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e97-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27e97-121">-ResourceGroupName</span></span>
<span data-ttu-id="27e97-122">Specifica il nome del gruppo di risorse a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="27e97-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e97-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e97-123">CommonParameters</span></span>
<span data-ttu-id="27e97-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27e97-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e97-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27e97-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e97-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27e97-126">INPUTS</span></span>

### <span data-ttu-id="27e97-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="27e97-127">PSEndpoint</span></span>
<span data-ttu-id="27e97-128">Il parametro ' CdnEndpoint ' accetta il valore di tipo ' PSEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="27e97-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="27e97-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27e97-129">OUTPUTS</span></span>

###  
<span data-ttu-id="27e97-130">Questo cmdlet restituisce un oggetto server di origine.</span><span class="sxs-lookup"><span data-stu-id="27e97-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="27e97-131">Note</span><span class="sxs-lookup"><span data-stu-id="27e97-131">NOTES</span></span>

## <span data-ttu-id="27e97-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27e97-132">RELATED LINKS</span></span>

[<span data-ttu-id="27e97-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="27e97-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


