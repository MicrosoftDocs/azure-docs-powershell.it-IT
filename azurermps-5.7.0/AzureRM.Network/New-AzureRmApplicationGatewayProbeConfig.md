---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 955f5179340351dd662979385ca3d3dc2a39b9f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519414"
---
# <span data-ttu-id="39275-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="39275-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="39275-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39275-102">SYNOPSIS</span></span>
<span data-ttu-id="39275-103">Crea una sonda di integrità.</span><span class="sxs-lookup"><span data-stu-id="39275-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39275-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39275-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39275-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39275-105">DESCRIPTION</span></span>
<span data-ttu-id="39275-106">Il cmdlet New-AzureRmApplicationGatewayProbeConfig crea una sonda di integrità.</span><span class="sxs-lookup"><span data-stu-id="39275-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="39275-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39275-107">EXAMPLES</span></span>

### <span data-ttu-id="39275-108">Esempio1: creare una sonda di integrità</span><span class="sxs-lookup"><span data-stu-id="39275-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="39275-109">Questo comando crea una sonda di integrità denominata Probe03, con protocollo HTTP, un intervallo di 30 secondi, un timeout di 120 secondi e una soglia non sana di 8 tentativi.</span><span class="sxs-lookup"><span data-stu-id="39275-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="39275-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39275-110">PARAMETERS</span></span>

### <span data-ttu-id="39275-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39275-111">-DefaultProfile</span></span>
<span data-ttu-id="39275-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39275-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39275-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="39275-113">-HostName</span></span>
<span data-ttu-id="39275-114">Specifica il nome host che questo cmdlet invia al Probe.</span><span class="sxs-lookup"><span data-stu-id="39275-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="39275-115">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="39275-115">-Interval</span></span>
<span data-ttu-id="39275-116">Specifica l'intervallo di probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="39275-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="39275-117">Questo è l'intervallo di tempo tra due sonde consecutive.</span><span class="sxs-lookup"><span data-stu-id="39275-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="39275-118">Questo valore è compreso tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="39275-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="39275-119">-Match</span><span class="sxs-lookup"><span data-stu-id="39275-119">-Match</span></span>
<span data-ttu-id="39275-120">Corpo che deve essere contenuto nella risposta di integrità.</span><span class="sxs-lookup"><span data-stu-id="39275-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="39275-121">Il valore predefinito è Empty</span><span class="sxs-lookup"><span data-stu-id="39275-121">Default value is empty</span></span>

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

### <span data-ttu-id="39275-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="39275-122">-MinServers</span></span>
<span data-ttu-id="39275-123">Numero minimo di server sempre contrassegnati come integri.</span><span class="sxs-lookup"><span data-stu-id="39275-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="39275-124">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="39275-124">Default value is 0</span></span>

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

### <span data-ttu-id="39275-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="39275-125">-Name</span></span>
<span data-ttu-id="39275-126">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="39275-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="39275-127">-Path</span><span class="sxs-lookup"><span data-stu-id="39275-127">-Path</span></span>
<span data-ttu-id="39275-128">Specifica il percorso relativo di probe.</span><span class="sxs-lookup"><span data-stu-id="39275-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="39275-129">I percorsi validi iniziano con il carattere barra (/).</span><span class="sxs-lookup"><span data-stu-id="39275-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="39275-130">Il probe viene inviato a \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="39275-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="39275-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="39275-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="39275-132">Se l'intestazione host deve essere selezionata dalle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="39275-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="39275-133">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="39275-133">Default value is false</span></span>

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

### <span data-ttu-id="39275-134">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="39275-134">-Protocol</span></span>
<span data-ttu-id="39275-135">Specifica il protocollo usato per inviare Probe.</span><span class="sxs-lookup"><span data-stu-id="39275-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="39275-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="39275-136">-Timeout</span></span>
<span data-ttu-id="39275-137">Specifica il timeout del probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="39275-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="39275-138">Questo cmdlet contrassegna la sonda come non riuscita se non viene ricevuta una risposta valida con questo periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="39275-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="39275-139">I valori validi sono compresi tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="39275-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="39275-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="39275-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="39275-141">Specifica il numero di tentativi di probe.</span><span class="sxs-lookup"><span data-stu-id="39275-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="39275-142">Il server back-end viene contrassegnato in basso dopo il conteggio errori consecutivi Probe raggiunge la soglia non sana.</span><span class="sxs-lookup"><span data-stu-id="39275-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="39275-143">I valori validi sono compresi tra 1 secondo e 20 secondi.</span><span class="sxs-lookup"><span data-stu-id="39275-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="39275-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39275-144">CommonParameters</span></span>
<span data-ttu-id="39275-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39275-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39275-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39275-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39275-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39275-147">INPUTS</span></span>

### <span data-ttu-id="39275-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="39275-148">None</span></span>
<span data-ttu-id="39275-149">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="39275-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="39275-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39275-150">OUTPUTS</span></span>

### <span data-ttu-id="39275-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="39275-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="39275-152">Note</span><span class="sxs-lookup"><span data-stu-id="39275-152">NOTES</span></span>

## <span data-ttu-id="39275-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39275-153">RELATED LINKS</span></span>

[<span data-ttu-id="39275-154">Creare una Probe personalizzata per il gateway applicazione usando PowerShell per gestione risorse di Azure</span><span class="sxs-lookup"><span data-stu-id="39275-154">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="39275-155">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="39275-155">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="39275-156">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="39275-156">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="39275-157">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="39275-157">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="39275-158">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="39275-158">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

