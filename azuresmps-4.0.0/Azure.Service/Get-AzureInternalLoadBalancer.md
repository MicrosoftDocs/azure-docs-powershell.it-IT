---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A439ADC4-991E-4860-82AA-7BED315991B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9f28659835fef4778eac729ccd020eb82f563bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029802"
---
# <span data-ttu-id="07349-101">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07349-101">Get-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="07349-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07349-102">SYNOPSIS</span></span>
<span data-ttu-id="07349-103">Ottiene i dettagli della configurazione interna del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="07349-103">Gets the details of the internal load balancer configuration.</span></span>

## <span data-ttu-id="07349-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07349-104">SYNTAX</span></span>

```
Get-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="07349-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07349-105">DESCRIPTION</span></span>
<span data-ttu-id="07349-106">Il cmdlet **Get-AzureInternalLoadBalancer** ottiene i dettagli della configurazione di bilanciamento del carico interna per un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="07349-106">The **Get-AzureInternalLoadBalancer** cmdlet gets the details of the internal load balancer configuration for an Azure service.</span></span>

## <span data-ttu-id="07349-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07349-107">EXAMPLES</span></span>

### <span data-ttu-id="07349-108">Esempio 1: ottenere informazioni dettagliate per un bilanciamento del carico interno</span><span class="sxs-lookup"><span data-stu-id="07349-108">Example 1: Get details for an internal load balancer</span></span>
```
PS C:\> Get-AzureService -ServiceName "ContosoService" | Get-AzureInternalLoadBalancer
```

<span data-ttu-id="07349-109">Questo comando ottiene il servizio denominato ContosoService usando il cmdlet **Get-AzureService** .</span><span class="sxs-lookup"><span data-stu-id="07349-109">This command gets the service named ContosoService by using the **Get-AzureService** cmdlet.</span></span>
<span data-ttu-id="07349-110">Il comando passa il servizio al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="07349-110">The command passes that service to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="07349-111">Il cmdlet corrente ottiene i dettagli per il servizio di bilanciamento del carico interno per tale Service.</span><span class="sxs-lookup"><span data-stu-id="07349-111">The current cmdlet gets details for the internal load balancer for that service.</span></span>

## <span data-ttu-id="07349-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07349-112">PARAMETERS</span></span>

### <span data-ttu-id="07349-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="07349-113">-InformationAction</span></span>
<span data-ttu-id="07349-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="07349-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="07349-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="07349-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07349-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="07349-116">Continue</span></span>
- <span data-ttu-id="07349-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="07349-117">Ignore</span></span>
- <span data-ttu-id="07349-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="07349-118">Inquire</span></span>
- <span data-ttu-id="07349-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="07349-119">SilentlyContinue</span></span>
- <span data-ttu-id="07349-120">Stop</span><span class="sxs-lookup"><span data-stu-id="07349-120">Stop</span></span>
- <span data-ttu-id="07349-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="07349-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07349-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="07349-122">-InformationVariable</span></span>
<span data-ttu-id="07349-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="07349-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07349-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="07349-124">-Profile</span></span>
<span data-ttu-id="07349-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07349-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="07349-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="07349-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07349-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="07349-127">-ServiceName</span></span>
<span data-ttu-id="07349-128">Specifica il nome del servizio per il quale questo cmdlet ottiene i dettagli per un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="07349-128">Specifies the name of the service for which this cmdlet gets details for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07349-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07349-129">CommonParameters</span></span>
<span data-ttu-id="07349-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07349-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07349-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07349-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07349-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07349-132">INPUTS</span></span>

## <span data-ttu-id="07349-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07349-133">OUTPUTS</span></span>

### <span data-ttu-id="07349-134">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. InternalLoadBalancerContext</span><span class="sxs-lookup"><span data-stu-id="07349-134">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerContext</span></span>

## <span data-ttu-id="07349-135">Note</span><span class="sxs-lookup"><span data-stu-id="07349-135">NOTES</span></span>

## <span data-ttu-id="07349-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07349-136">RELATED LINKS</span></span>

[<span data-ttu-id="07349-137">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07349-137">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="07349-138">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="07349-138">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="07349-139">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="07349-139">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="07349-140">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07349-140">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="07349-141">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07349-141">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


