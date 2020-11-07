---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 43c74d2edd2cfd07f65b7d5437bf1cf5c0dfca9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860561"
---
# <span data-ttu-id="16bae-101">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16bae-101">New-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="16bae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16bae-102">SYNOPSIS</span></span>
<span data-ttu-id="16bae-103">Crea una sonda di integrità.</span><span class="sxs-lookup"><span data-stu-id="16bae-103">Creates a health probe.</span></span>

## <span data-ttu-id="16bae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16bae-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16bae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16bae-105">DESCRIPTION</span></span>
<span data-ttu-id="16bae-106">Il cmdlet New-AzApplicationGatewayProbeConfig crea una sonda di integrità.</span><span class="sxs-lookup"><span data-stu-id="16bae-106">The New-AzApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="16bae-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16bae-107">EXAMPLES</span></span>

### <span data-ttu-id="16bae-108">Esempio1: creare una sonda di integrità</span><span class="sxs-lookup"><span data-stu-id="16bae-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="16bae-109">Questo comando crea una sonda di integrità denominata Probe03, con protocollo HTTP, un intervallo di 30 secondi, un timeout di 120 secondi e una soglia non sana di 8 tentativi.</span><span class="sxs-lookup"><span data-stu-id="16bae-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="16bae-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16bae-110">PARAMETERS</span></span>

### <span data-ttu-id="16bae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16bae-111">-DefaultProfile</span></span>
<span data-ttu-id="16bae-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16bae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16bae-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="16bae-113">-HostName</span></span>
<span data-ttu-id="16bae-114">Specifica il nome host che questo cmdlet invia al Probe.</span><span class="sxs-lookup"><span data-stu-id="16bae-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="16bae-115">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="16bae-115">-Interval</span></span>
<span data-ttu-id="16bae-116">Specifica l'intervallo di probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="16bae-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="16bae-117">Questo è l'intervallo di tempo tra due sonde consecutive.</span><span class="sxs-lookup"><span data-stu-id="16bae-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="16bae-118">Questo valore è compreso tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="16bae-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="16bae-119">-Match</span><span class="sxs-lookup"><span data-stu-id="16bae-119">-Match</span></span>
<span data-ttu-id="16bae-120">Corpo che deve essere contenuto nella risposta di integrità.</span><span class="sxs-lookup"><span data-stu-id="16bae-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="16bae-121">Il valore predefinito è Empty</span><span class="sxs-lookup"><span data-stu-id="16bae-121">Default value is empty</span></span>

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16bae-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="16bae-122">-MinServers</span></span>
<span data-ttu-id="16bae-123">Numero minimo di server sempre contrassegnati come integri.</span><span class="sxs-lookup"><span data-stu-id="16bae-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="16bae-124">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="16bae-124">Default value is 0</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16bae-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="16bae-125">-Name</span></span>
<span data-ttu-id="16bae-126">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="16bae-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="16bae-127">-Path</span><span class="sxs-lookup"><span data-stu-id="16bae-127">-Path</span></span>
<span data-ttu-id="16bae-128">Specifica il percorso relativo di probe.</span><span class="sxs-lookup"><span data-stu-id="16bae-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="16bae-129">I percorsi validi iniziano con il carattere barra (/).</span><span class="sxs-lookup"><span data-stu-id="16bae-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="16bae-130">Il probe viene inviato al \< protocollo \> :// \< host \> : Path della \< porta \> \< \> .</span><span class="sxs-lookup"><span data-stu-id="16bae-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="16bae-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="16bae-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="16bae-132">Se l'intestazione host deve essere selezionata dalle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="16bae-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="16bae-133">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="16bae-133">Default value is false</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16bae-134">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="16bae-134">-Protocol</span></span>
<span data-ttu-id="16bae-135">Specifica il protocollo usato per inviare Probe.</span><span class="sxs-lookup"><span data-stu-id="16bae-135">Specifies the protocol used to send probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16bae-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="16bae-136">-Timeout</span></span>
<span data-ttu-id="16bae-137">Specifica il timeout del probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="16bae-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="16bae-138">Questo cmdlet contrassegna la sonda come non riuscita se non viene ricevuta una risposta valida con questo periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="16bae-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="16bae-139">I valori validi sono compresi tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="16bae-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="16bae-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="16bae-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="16bae-141">Specifica il numero di tentativi di probe.</span><span class="sxs-lookup"><span data-stu-id="16bae-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="16bae-142">Il server back-end viene contrassegnato in basso dopo il conteggio errori consecutivi Probe raggiunge la soglia non sana.</span><span class="sxs-lookup"><span data-stu-id="16bae-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="16bae-143">I valori validi sono compresi tra 1 secondo e 20 secondi.</span><span class="sxs-lookup"><span data-stu-id="16bae-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="16bae-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16bae-144">CommonParameters</span></span>
<span data-ttu-id="16bae-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16bae-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16bae-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16bae-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16bae-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16bae-147">INPUTS</span></span>

## <span data-ttu-id="16bae-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16bae-148">OUTPUTS</span></span>

### <span data-ttu-id="16bae-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="16bae-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="16bae-150">Note</span><span class="sxs-lookup"><span data-stu-id="16bae-150">NOTES</span></span>

## <span data-ttu-id="16bae-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16bae-151">RELATED LINKS</span></span>

[<span data-ttu-id="16bae-152">Creare una Probe personalizzata per il gateway applicazione usando PowerShell per gestione risorse di Azure</span><span class="sxs-lookup"><span data-stu-id="16bae-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="16bae-153">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16bae-153">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="16bae-154">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16bae-154">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="16bae-155">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16bae-155">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="16bae-156">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16bae-156">Set-AzApplicationGatewayProbeConfig</span></span>]()

