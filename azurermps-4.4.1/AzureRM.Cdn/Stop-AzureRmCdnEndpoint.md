---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 83229b9251e7cbbbe4bd17d73004b9bc64800511
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517011"
---
# <span data-ttu-id="b9a6a-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9a6a-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="b9a6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a6a-103">Interrompe l'endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="b9a6a-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9a6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9a6a-104">SYNTAX</span></span>

### <span data-ttu-id="b9a6a-105">Parametro set per i parametri dei campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9a6a-105">Parameter Set for fields parameters (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a6a-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="b9a6a-106">Parameter Set for object parameters</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9a6a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9a6a-107">DESCRIPTION</span></span>
<span data-ttu-id="b9a6a-108">Il cmdlet **Stop-AzureRmCdnEndpoint** arresta l'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="b9a6a-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b9a6a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9a6a-109">EXAMPLES</span></span>

## <span data-ttu-id="b9a6a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9a6a-110">PARAMETERS</span></span>

### <span data-ttu-id="b9a6a-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9a6a-111">-CdnEndpoint</span></span>
<span data-ttu-id="b9a6a-112">Specifica l'oggetto endpoint che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="b9a6a-112">Specifies the endpoint object that this cmdlet stops.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9a6a-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b9a6a-113">-EndpointName</span></span>
<span data-ttu-id="b9a6a-114">Specifica il nome dell'endpoint interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9a6a-114">Specifies the name of the endpoint that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a6a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9a6a-115">-PassThru</span></span>
<span data-ttu-id="b9a6a-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b9a6a-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b9a6a-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b9a6a-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b9a6a-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b9a6a-118">-ProfileName</span></span>
<span data-ttu-id="b9a6a-119">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="b9a6a-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a6a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a6a-120">-ResourceGroupName</span></span>
<span data-ttu-id="b9a6a-121">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="b9a6a-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a6a-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9a6a-122">-Confirm</span></span>
<span data-ttu-id="b9a6a-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9a6a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a6a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9a6a-124">-WhatIf</span></span>
<span data-ttu-id="b9a6a-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9a6a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9a6a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9a6a-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a6a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a6a-127">-DefaultProfile</span></span>
<span data-ttu-id="b9a6a-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9a6a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9a6a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a6a-129">CommonParameters</span></span>
<span data-ttu-id="b9a6a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a6a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a6a-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9a6a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a6a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9a6a-132">INPUTS</span></span>

### <span data-ttu-id="b9a6a-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9a6a-133">PSEndpoint</span></span>
<span data-ttu-id="b9a6a-134">Il parametro ' CdnEndpoint ' accetta il valore di tipo ' PSEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b9a6a-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="b9a6a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9a6a-135">OUTPUTS</span></span>

### <span data-ttu-id="b9a6a-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9a6a-136">System.Boolean</span></span>

## <span data-ttu-id="b9a6a-137">Note</span><span class="sxs-lookup"><span data-stu-id="b9a6a-137">NOTES</span></span>

## <span data-ttu-id="b9a6a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9a6a-138">RELATED LINKS</span></span>

[<span data-ttu-id="b9a6a-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9a6a-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b9a6a-140">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9a6a-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b9a6a-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9a6a-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b9a6a-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9a6a-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b9a6a-143">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9a6a-143">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


