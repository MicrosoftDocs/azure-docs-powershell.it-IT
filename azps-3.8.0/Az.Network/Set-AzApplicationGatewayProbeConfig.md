---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: e7da21709215b4ab185a573e32c8d15de901b33f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022784"
---
# <span data-ttu-id="e05bb-101">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e05bb-101">Set-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="e05bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e05bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e05bb-103">Imposta la configurazione della sonda integrità in un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="e05bb-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="e05bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e05bb-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e05bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e05bb-105">DESCRIPTION</span></span>
<span data-ttu-id="e05bb-106">Il cmdlet Set-AzApplicationGatewayProbeConfig imposta la configurazione della sonda di integrità in un gateway di applicazioni esistente.</span><span class="sxs-lookup"><span data-stu-id="e05bb-106">The Set-AzApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="e05bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e05bb-107">EXAMPLES</span></span>

### <span data-ttu-id="e05bb-108">Esempio 1: impostare la configurazione di una sonda di integrità in un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="e05bb-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="e05bb-109">Questo comando imposta la configurazione di una sonda di integrità denominata Probe05 per il gateway dell'applicazione denominata gateway.</span><span class="sxs-lookup"><span data-stu-id="e05bb-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="e05bb-110">Il comando imposta anche la soglia non sana su 8 tentativi e timeout dopo 120 secondi.</span><span class="sxs-lookup"><span data-stu-id="e05bb-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="e05bb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e05bb-111">PARAMETERS</span></span>

### <span data-ttu-id="e05bb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e05bb-112">-ApplicationGateway</span></span>
<span data-ttu-id="e05bb-113">Specifica il gateway dell'applicazione a cui questo cmdlet invia un probe.</span><span class="sxs-lookup"><span data-stu-id="e05bb-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e05bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05bb-114">-DefaultProfile</span></span>
<span data-ttu-id="e05bb-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e05bb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e05bb-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="e05bb-116">-HostName</span></span>
<span data-ttu-id="e05bb-117">Specifica il nome host a cui il cmdlet invia il probe.</span><span class="sxs-lookup"><span data-stu-id="e05bb-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="e05bb-118">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="e05bb-118">-Interval</span></span>
<span data-ttu-id="e05bb-119">Specifica l'intervallo di probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="e05bb-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="e05bb-120">Questo è l'intervallo di tempo tra due sonde consecutive.</span><span class="sxs-lookup"><span data-stu-id="e05bb-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="e05bb-121">Questo valore è compreso tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="e05bb-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e05bb-122">-Match</span><span class="sxs-lookup"><span data-stu-id="e05bb-122">-Match</span></span>
<span data-ttu-id="e05bb-123">Corpo che deve essere contenuto nella risposta di integrità.</span><span class="sxs-lookup"><span data-stu-id="e05bb-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="e05bb-124">Il valore predefinito è Empty</span><span class="sxs-lookup"><span data-stu-id="e05bb-124">Default value is empty</span></span>

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

### <span data-ttu-id="e05bb-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="e05bb-125">-MinServers</span></span>
<span data-ttu-id="e05bb-126">Numero minimo di server sempre contrassegnati come integri.</span><span class="sxs-lookup"><span data-stu-id="e05bb-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="e05bb-127">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="e05bb-127">Default value is 0</span></span>

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

### <span data-ttu-id="e05bb-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e05bb-128">-Name</span></span>
<span data-ttu-id="e05bb-129">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="e05bb-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="e05bb-130">-Path</span><span class="sxs-lookup"><span data-stu-id="e05bb-130">-Path</span></span>
<span data-ttu-id="e05bb-131">Specifica il percorso relativo di probe.</span><span class="sxs-lookup"><span data-stu-id="e05bb-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="e05bb-132">I percorsi validi iniziano con il carattere barra (/).</span><span class="sxs-lookup"><span data-stu-id="e05bb-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="e05bb-133">Il probe viene inviato al \< protocollo \> :// \< host \> : Path della \< porta \> \< \> .</span><span class="sxs-lookup"><span data-stu-id="e05bb-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="e05bb-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e05bb-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="e05bb-135">Se l'intestazione host deve essere selezionata dalle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="e05bb-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="e05bb-136">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="e05bb-136">Default value is false</span></span>

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

### <span data-ttu-id="e05bb-137">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="e05bb-137">-Protocol</span></span>
<span data-ttu-id="e05bb-138">Specifica il protocollo usato per inviare Probe.</span><span class="sxs-lookup"><span data-stu-id="e05bb-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="e05bb-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="e05bb-139">-Timeout</span></span>
<span data-ttu-id="e05bb-140">Specifica il timeout del probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="e05bb-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="e05bb-141">Questo cmdlet contrassegna la sonda come non riuscita se non viene ricevuta una risposta valida con questo periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="e05bb-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="e05bb-142">I valori validi sono compresi tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="e05bb-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e05bb-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="e05bb-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="e05bb-144">Specifica il numero di tentativi di probe.</span><span class="sxs-lookup"><span data-stu-id="e05bb-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="e05bb-145">Il server back-end viene contrassegnato in basso dopo il conteggio errori consecutivi Probe raggiunge la soglia non sana.</span><span class="sxs-lookup"><span data-stu-id="e05bb-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="e05bb-146">I valori validi sono compresi tra 1 secondo e 20 secondi.</span><span class="sxs-lookup"><span data-stu-id="e05bb-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="e05bb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05bb-147">CommonParameters</span></span>
<span data-ttu-id="e05bb-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05bb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05bb-149">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05bb-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05bb-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e05bb-150">INPUTS</span></span>

### <span data-ttu-id="e05bb-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e05bb-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e05bb-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e05bb-152">OUTPUTS</span></span>

### <span data-ttu-id="e05bb-153">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e05bb-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e05bb-154">Note</span><span class="sxs-lookup"><span data-stu-id="e05bb-154">NOTES</span></span>

## <span data-ttu-id="e05bb-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e05bb-155">RELATED LINKS</span></span>

[<span data-ttu-id="e05bb-156">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e05bb-156">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="e05bb-157">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e05bb-157">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="e05bb-158">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e05bb-158">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="e05bb-159">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e05bb-159">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

