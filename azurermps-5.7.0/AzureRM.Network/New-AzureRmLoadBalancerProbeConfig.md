---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 0e5216f88cc860244cf11a693a73e30ba6e83390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518919"
---
# <span data-ttu-id="81808-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="81808-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="81808-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81808-102">SYNOPSIS</span></span>
<span data-ttu-id="81808-103">Crea una configurazione Probe per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="81808-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81808-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81808-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81808-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81808-105">DESCRIPTION</span></span>
<span data-ttu-id="81808-106">Il cmdlet **New-AzureRmLoadBalancerProbeConfig** crea una configurazione di probe per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="81808-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="81808-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81808-107">EXAMPLES</span></span>

### <span data-ttu-id="81808-108">Esempio 1: creare una configurazione Probe</span><span class="sxs-lookup"><span data-stu-id="81808-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="81808-109">Questo comando crea una configurazione di probe denominata Probe usando il protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="81808-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="81808-110">La nuova sonda si connette a un servizio con bilanciamento del carico sulla porta 80.</span><span class="sxs-lookup"><span data-stu-id="81808-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="81808-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81808-111">PARAMETERS</span></span>

### <span data-ttu-id="81808-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81808-112">-DefaultProfile</span></span>
<span data-ttu-id="81808-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81808-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81808-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="81808-114">-IntervalInSeconds</span></span>
<span data-ttu-id="81808-115">Specifica l'intervallo, in secondi, tra le sonde per ogni istanza di un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="81808-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="81808-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="81808-116">-Name</span></span>
<span data-ttu-id="81808-117">Specifica il nome della configurazione del Probe da creare.</span><span class="sxs-lookup"><span data-stu-id="81808-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="81808-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="81808-118">-Port</span></span>
<span data-ttu-id="81808-119">Specifica la porta in cui la nuova sonda deve connettersi a un servizio con bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="81808-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="81808-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="81808-120">-ProbeCount</span></span>
<span data-ttu-id="81808-121">Specifica il numero di errori consecutivi per istanza per un'istanza da considerare non sani.</span><span class="sxs-lookup"><span data-stu-id="81808-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="81808-122">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="81808-122">-Protocol</span></span>
<span data-ttu-id="81808-123">Specifica il protocollo da usare per la configurazione del probe.</span><span class="sxs-lookup"><span data-stu-id="81808-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="81808-124">I valori accettabili per questo parametro sono: TCP o http.</span><span class="sxs-lookup"><span data-stu-id="81808-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="81808-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="81808-125">-RequestPath</span></span>
<span data-ttu-id="81808-126">Specifica il percorso in un servizio con bilanciamento del carico da sondare per determinare l'integrità.</span><span class="sxs-lookup"><span data-stu-id="81808-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="81808-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81808-127">CommonParameters</span></span>
<span data-ttu-id="81808-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81808-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81808-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81808-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81808-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81808-130">INPUTS</span></span>

### <span data-ttu-id="81808-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="81808-131">None</span></span>
<span data-ttu-id="81808-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="81808-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="81808-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81808-133">OUTPUTS</span></span>

### <span data-ttu-id="81808-134">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="81808-134">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="81808-135">Note</span><span class="sxs-lookup"><span data-stu-id="81808-135">NOTES</span></span>

## <span data-ttu-id="81808-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81808-136">RELATED LINKS</span></span>

[<span data-ttu-id="81808-137">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="81808-137">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="81808-138">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="81808-138">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="81808-139">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="81808-139">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="81808-140">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="81808-140">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


