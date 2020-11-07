---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 75688743c03db16c9683b84698ad41ddcb7fa52e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678355"
---
# <span data-ttu-id="58f7d-101">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="58f7d-101">New-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="58f7d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="58f7d-103">Crea una sonda di integrità.</span><span class="sxs-lookup"><span data-stu-id="58f7d-103">Creates a health probe.</span></span>

## <span data-ttu-id="58f7d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58f7d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58f7d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="58f7d-106">Il cmdlet New-AzApplicationGatewayProbeConfig crea una sonda di integrità.</span><span class="sxs-lookup"><span data-stu-id="58f7d-106">The New-AzApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="58f7d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58f7d-107">EXAMPLES</span></span>

### <span data-ttu-id="58f7d-108">Esempio1: creare una sonda di integrità</span><span class="sxs-lookup"><span data-stu-id="58f7d-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="58f7d-109">Questo comando crea una sonda di integrità denominata Probe03, con protocollo HTTP, un intervallo di 30 secondi, un timeout di 120 secondi e una soglia non sana di 8 tentativi.</span><span class="sxs-lookup"><span data-stu-id="58f7d-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="58f7d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58f7d-110">PARAMETERS</span></span>

### <span data-ttu-id="58f7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f7d-111">-DefaultProfile</span></span>
<span data-ttu-id="58f7d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58f7d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58f7d-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="58f7d-113">-HostName</span></span>
<span data-ttu-id="58f7d-114">Specifica il nome host che questo cmdlet invia al Probe.</span><span class="sxs-lookup"><span data-stu-id="58f7d-114">Specifies the host name that this cmdlet sends the probe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f7d-115">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="58f7d-115">-Interval</span></span>
<span data-ttu-id="58f7d-116">Specifica l'intervallo di probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="58f7d-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="58f7d-117">Questo è l'intervallo di tempo tra due sonde consecutive.</span><span class="sxs-lookup"><span data-stu-id="58f7d-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="58f7d-118">Questo valore è compreso tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="58f7d-118">This value is between 1 second and 86400 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f7d-119">-Match</span><span class="sxs-lookup"><span data-stu-id="58f7d-119">-Match</span></span>
<span data-ttu-id="58f7d-120">Corpo che deve essere contenuto nella risposta di integrità.</span><span class="sxs-lookup"><span data-stu-id="58f7d-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="58f7d-121">Il valore predefinito è Empty</span><span class="sxs-lookup"><span data-stu-id="58f7d-121">Default value is empty</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f7d-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="58f7d-122">-MinServers</span></span>
<span data-ttu-id="58f7d-123">Numero minimo di server sempre contrassegnati come integri.</span><span class="sxs-lookup"><span data-stu-id="58f7d-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="58f7d-124">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="58f7d-124">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f7d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="58f7d-125">-Name</span></span>
<span data-ttu-id="58f7d-126">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="58f7d-126">Specifies the name of the probe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f7d-127">-Path</span><span class="sxs-lookup"><span data-stu-id="58f7d-127">-Path</span></span>
<span data-ttu-id="58f7d-128">Specifica il percorso relativo di probe.</span><span class="sxs-lookup"><span data-stu-id="58f7d-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="58f7d-129">I percorsi validi iniziano con il carattere barra (/).</span><span class="sxs-lookup"><span data-stu-id="58f7d-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="58f7d-130">Il probe viene inviato al \< protocollo \> :// \< host \> : Path della \< porta \> \< \> .</span><span class="sxs-lookup"><span data-stu-id="58f7d-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f7d-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="58f7d-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="58f7d-132">Se l'intestazione host deve essere selezionata dalle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="58f7d-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="58f7d-133">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="58f7d-133">Default value is false</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f7d-134">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="58f7d-134">-Protocol</span></span>
<span data-ttu-id="58f7d-135">Specifica il protocollo usato per inviare Probe.</span><span class="sxs-lookup"><span data-stu-id="58f7d-135">Specifies the protocol used to send probe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f7d-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="58f7d-136">-Timeout</span></span>
<span data-ttu-id="58f7d-137">Specifica il timeout del probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="58f7d-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="58f7d-138">Questo cmdlet contrassegna la sonda come non riuscita se non viene ricevuta una risposta valida con questo periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="58f7d-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="58f7d-139">I valori validi sono compresi tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="58f7d-139">Valid values are between 1 second and 86400 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f7d-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="58f7d-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="58f7d-141">Specifica il numero di tentativi di probe.</span><span class="sxs-lookup"><span data-stu-id="58f7d-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="58f7d-142">Il server back-end viene contrassegnato in basso dopo il conteggio errori consecutivi Probe raggiunge la soglia non sana.</span><span class="sxs-lookup"><span data-stu-id="58f7d-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="58f7d-143">I valori validi sono compresi tra 1 secondo e 20 secondi.</span><span class="sxs-lookup"><span data-stu-id="58f7d-143">Valid values are between 1 second and 20 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f7d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f7d-144">CommonParameters</span></span>
<span data-ttu-id="58f7d-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58f7d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f7d-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58f7d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f7d-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58f7d-147">INPUTS</span></span>

### <span data-ttu-id="58f7d-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="58f7d-148">None</span></span>

## <span data-ttu-id="58f7d-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58f7d-149">OUTPUTS</span></span>

### <span data-ttu-id="58f7d-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="58f7d-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="58f7d-151">Note</span><span class="sxs-lookup"><span data-stu-id="58f7d-151">NOTES</span></span>

## <span data-ttu-id="58f7d-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58f7d-152">RELATED LINKS</span></span>

[<span data-ttu-id="58f7d-153">Creare una Probe personalizzata per il gateway applicazione usando PowerShell per gestione risorse di Azure</span><span class="sxs-lookup"><span data-stu-id="58f7d-153">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="58f7d-154">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="58f7d-154">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="58f7d-155">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="58f7d-155">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="58f7d-156">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="58f7d-156">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="58f7d-157">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="58f7d-157">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

