---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 30a717d24145364f2850a381382e8d7d35303172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687784"
---
# <span data-ttu-id="0c87b-101">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c87b-101">Set-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="0c87b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c87b-102">SYNOPSIS</span></span>
<span data-ttu-id="0c87b-103">Imposta la configurazione della sonda integrità in un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="0c87b-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c87b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c87b-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c87b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c87b-105">DESCRIPTION</span></span>
<span data-ttu-id="0c87b-106">Il cmdlet Set-AzureRmApplicationGatewayProbeConfig imposta la configurazione della sonda di integrità in un gateway di applicazioni esistente.</span><span class="sxs-lookup"><span data-stu-id="0c87b-106">The Set-AzureRmApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="0c87b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c87b-107">EXAMPLES</span></span>

### <span data-ttu-id="0c87b-108">Esempio 1: impostare la configurazione di una sonda di integrità in un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="0c87b-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="0c87b-109">Questo comando imposta la configurazione di una sonda di integrità denominata Probe05 per il gateway dell'applicazione denominata gateway.</span><span class="sxs-lookup"><span data-stu-id="0c87b-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="0c87b-110">Il comando imposta anche la soglia non sana su 8 tentativi e timeout dopo 120 secondi.</span><span class="sxs-lookup"><span data-stu-id="0c87b-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="0c87b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c87b-111">PARAMETERS</span></span>

### <span data-ttu-id="0c87b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c87b-112">-ApplicationGateway</span></span>
<span data-ttu-id="0c87b-113">Specifica il gateway dell'applicazione a cui questo cmdlet invia un probe.</span><span class="sxs-lookup"><span data-stu-id="0c87b-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="0c87b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c87b-114">-DefaultProfile</span></span>
<span data-ttu-id="0c87b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c87b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c87b-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="0c87b-116">-HostName</span></span>
<span data-ttu-id="0c87b-117">Specifica il nome host a cui il cmdlet invia il probe.</span><span class="sxs-lookup"><span data-stu-id="0c87b-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="0c87b-118">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="0c87b-118">-Interval</span></span>
<span data-ttu-id="0c87b-119">Specifica l'intervallo di probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="0c87b-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="0c87b-120">Questo è l'intervallo di tempo tra due sonde consecutive.</span><span class="sxs-lookup"><span data-stu-id="0c87b-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="0c87b-121">Questo valore è compreso tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="0c87b-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="0c87b-122">-Match</span><span class="sxs-lookup"><span data-stu-id="0c87b-122">-Match</span></span>
<span data-ttu-id="0c87b-123">Corpo che deve essere contenuto nella risposta di integrità.</span><span class="sxs-lookup"><span data-stu-id="0c87b-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="0c87b-124">Il valore predefinito è Empty</span><span class="sxs-lookup"><span data-stu-id="0c87b-124">Default value is empty</span></span>

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

### <span data-ttu-id="0c87b-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="0c87b-125">-MinServers</span></span>
<span data-ttu-id="0c87b-126">Numero minimo di server sempre contrassegnati come integri.</span><span class="sxs-lookup"><span data-stu-id="0c87b-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="0c87b-127">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="0c87b-127">Default value is 0</span></span>

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

### <span data-ttu-id="0c87b-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c87b-128">-Name</span></span>
<span data-ttu-id="0c87b-129">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="0c87b-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="0c87b-130">-Path</span><span class="sxs-lookup"><span data-stu-id="0c87b-130">-Path</span></span>
<span data-ttu-id="0c87b-131">Specifica il percorso relativo di probe.</span><span class="sxs-lookup"><span data-stu-id="0c87b-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="0c87b-132">I percorsi validi iniziano con il carattere barra (/).</span><span class="sxs-lookup"><span data-stu-id="0c87b-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="0c87b-133">Il probe viene inviato a \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="0c87b-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="0c87b-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0c87b-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="0c87b-135">Se l'intestazione host deve essere selezionata dalle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="0c87b-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="0c87b-136">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="0c87b-136">Default value is false</span></span>

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

### <span data-ttu-id="0c87b-137">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="0c87b-137">-Protocol</span></span>
<span data-ttu-id="0c87b-138">Specifica il protocollo usato per inviare Probe.</span><span class="sxs-lookup"><span data-stu-id="0c87b-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="0c87b-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="0c87b-139">-Timeout</span></span>
<span data-ttu-id="0c87b-140">Specifica il timeout del probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="0c87b-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="0c87b-141">Questo cmdlet contrassegna la sonda come non riuscita se non viene ricevuta una risposta valida con questo periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="0c87b-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="0c87b-142">I valori validi sono compresi tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="0c87b-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="0c87b-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="0c87b-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="0c87b-144">Specifica il numero di tentativi di probe.</span><span class="sxs-lookup"><span data-stu-id="0c87b-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="0c87b-145">Il server back-end viene contrassegnato in basso dopo il conteggio errori consecutivi Probe raggiunge la soglia non sana.</span><span class="sxs-lookup"><span data-stu-id="0c87b-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="0c87b-146">I valori validi sono compresi tra 1 secondo e 20 secondi.</span><span class="sxs-lookup"><span data-stu-id="0c87b-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="0c87b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c87b-147">CommonParameters</span></span>
<span data-ttu-id="0c87b-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c87b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c87b-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c87b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c87b-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c87b-150">INPUTS</span></span>

### <span data-ttu-id="0c87b-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c87b-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="0c87b-152">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c87b-152">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="0c87b-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c87b-153">OUTPUTS</span></span>

### <span data-ttu-id="0c87b-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c87b-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c87b-155">Note</span><span class="sxs-lookup"><span data-stu-id="0c87b-155">NOTES</span></span>

## <span data-ttu-id="0c87b-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c87b-156">RELATED LINKS</span></span>

[<span data-ttu-id="0c87b-157">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c87b-157">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0c87b-158">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c87b-158">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0c87b-159">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c87b-159">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0c87b-160">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c87b-160">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

