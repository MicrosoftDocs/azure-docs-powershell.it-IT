---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: f1d5ac87cc237e5a8ec92262255e996741346613
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867018"
---
# <span data-ttu-id="31ce2-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="31ce2-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="31ce2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="31ce2-103">Crea una configurazione Probe per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="31ce2-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31ce2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31ce2-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31ce2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31ce2-105">DESCRIPTION</span></span>
<span data-ttu-id="31ce2-106">Il cmdlet **New-AzureRmLoadBalancerProbeConfig** crea una configurazione di probe per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="31ce2-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="31ce2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31ce2-107">EXAMPLES</span></span>

### <span data-ttu-id="31ce2-108">Esempio 1: creare una configurazione Probe</span><span class="sxs-lookup"><span data-stu-id="31ce2-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="31ce2-109">Questo comando crea una configurazione di probe denominata Probe usando il protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="31ce2-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="31ce2-110">La nuova sonda si connette a un servizio con bilanciamento del carico sulla porta 80.</span><span class="sxs-lookup"><span data-stu-id="31ce2-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="31ce2-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31ce2-111">PARAMETERS</span></span>

### <span data-ttu-id="31ce2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ce2-112">-DefaultProfile</span></span>
<span data-ttu-id="31ce2-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31ce2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31ce2-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="31ce2-114">-IntervalInSeconds</span></span>
<span data-ttu-id="31ce2-115">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza di un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="31ce2-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ce2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="31ce2-116">-Name</span></span>
<span data-ttu-id="31ce2-117">Specifica il nome della configurazione del Probe da creare.</span><span class="sxs-lookup"><span data-stu-id="31ce2-117">Specifies the name of the probe configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ce2-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="31ce2-118">-Port</span></span>
<span data-ttu-id="31ce2-119">Specifica la porta in cui la nuova sonda deve connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="31ce2-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ce2-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="31ce2-120">-ProbeCount</span></span>
<span data-ttu-id="31ce2-121">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="31ce2-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ce2-122">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="31ce2-122">-Protocol</span></span>
<span data-ttu-id="31ce2-123">Specifica il protocollo da usare per la configurazione del probe.</span><span class="sxs-lookup"><span data-stu-id="31ce2-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="31ce2-124">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="31ce2-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ce2-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="31ce2-125">-RequestPath</span></span>
<span data-ttu-id="31ce2-126">Specifica il percorso in un servizio con bilanciamento del carico da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="31ce2-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="31ce2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ce2-127">CommonParameters</span></span>
<span data-ttu-id="31ce2-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ce2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ce2-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ce2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ce2-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31ce2-130">INPUTS</span></span>

## <span data-ttu-id="31ce2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31ce2-131">OUTPUTS</span></span>

### <span data-ttu-id="31ce2-132">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="31ce2-132">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="31ce2-133">Note</span><span class="sxs-lookup"><span data-stu-id="31ce2-133">NOTES</span></span>

## <span data-ttu-id="31ce2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31ce2-134">RELATED LINKS</span></span>

[<span data-ttu-id="31ce2-135">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="31ce2-135">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="31ce2-136">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="31ce2-136">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="31ce2-137">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="31ce2-137">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="31ce2-138">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="31ce2-138">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


