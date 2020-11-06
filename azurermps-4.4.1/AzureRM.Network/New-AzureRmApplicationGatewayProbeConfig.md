---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: a41daa12a126e768a4cc7842a72b031d4ca7a759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520495"
---
# <span data-ttu-id="d59c1-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d59c1-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="d59c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d59c1-102">SYNOPSIS</span></span>
<span data-ttu-id="d59c1-103">Crea una sonda di integrità.</span><span class="sxs-lookup"><span data-stu-id="d59c1-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d59c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d59c1-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d59c1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d59c1-105">DESCRIPTION</span></span>
<span data-ttu-id="d59c1-106">Il cmdlet New-AzureRmApplicationGatewayProbeConfig crea una sonda di integrità.</span><span class="sxs-lookup"><span data-stu-id="d59c1-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="d59c1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d59c1-107">EXAMPLES</span></span>

### <span data-ttu-id="d59c1-108">Esempio1: creare una sonda di integrità</span><span class="sxs-lookup"><span data-stu-id="d59c1-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="d59c1-109">Questo comando crea una sonda di integrità denominata Probe03, con protocollo HTTP, un intervallo di 30 secondi, un timeout di 120 secondi e una soglia non sana di 8 tentativi.</span><span class="sxs-lookup"><span data-stu-id="d59c1-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="d59c1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d59c1-110">PARAMETERS</span></span>

### <span data-ttu-id="d59c1-111">-HostName</span><span class="sxs-lookup"><span data-stu-id="d59c1-111">-HostName</span></span>
<span data-ttu-id="d59c1-112">Specifica il nome host che questo cmdlet invia al Probe.</span><span class="sxs-lookup"><span data-stu-id="d59c1-112">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="d59c1-113">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="d59c1-113">-Interval</span></span>
<span data-ttu-id="d59c1-114">Specifica l'intervallo di probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="d59c1-114">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="d59c1-115">Questo è l'intervallo di tempo tra due sonde consecutive.</span><span class="sxs-lookup"><span data-stu-id="d59c1-115">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="d59c1-116">Questo valore è compreso tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="d59c1-116">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="d59c1-117">-Match</span><span class="sxs-lookup"><span data-stu-id="d59c1-117">-Match</span></span>
<span data-ttu-id="d59c1-118">Corpo che deve essere contenuto nella risposta di integrità.</span><span class="sxs-lookup"><span data-stu-id="d59c1-118">Body that must be contained in the health response.</span></span>
<span data-ttu-id="d59c1-119">Il valore predefinito è Empty</span><span class="sxs-lookup"><span data-stu-id="d59c1-119">Default value is empty</span></span>

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

### <span data-ttu-id="d59c1-120">-MinServers</span><span class="sxs-lookup"><span data-stu-id="d59c1-120">-MinServers</span></span>
<span data-ttu-id="d59c1-121">Numero minimo di server sempre contrassegnati come integri.</span><span class="sxs-lookup"><span data-stu-id="d59c1-121">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="d59c1-122">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="d59c1-122">Default value is 0</span></span>

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

### <span data-ttu-id="d59c1-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d59c1-123">-Name</span></span>
<span data-ttu-id="d59c1-124">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="d59c1-124">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="d59c1-125">-Path</span><span class="sxs-lookup"><span data-stu-id="d59c1-125">-Path</span></span>
<span data-ttu-id="d59c1-126">Specifica il percorso relativo di probe.</span><span class="sxs-lookup"><span data-stu-id="d59c1-126">Specifies the relative path of probe.</span></span>
<span data-ttu-id="d59c1-127">I percorsi validi iniziano con il carattere barra (/).</span><span class="sxs-lookup"><span data-stu-id="d59c1-127">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="d59c1-128">Il probe viene inviato a \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="d59c1-128">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="d59c1-129">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d59c1-129">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="d59c1-130">Se l'intestazione host deve essere selezionata dalle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="d59c1-130">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="d59c1-131">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="d59c1-131">Default value is false</span></span>

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

### <span data-ttu-id="d59c1-132">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="d59c1-132">-Protocol</span></span>
<span data-ttu-id="d59c1-133">Specifica il protocollo usato per inviare Probe.</span><span class="sxs-lookup"><span data-stu-id="d59c1-133">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="d59c1-134">-Timeout</span><span class="sxs-lookup"><span data-stu-id="d59c1-134">-Timeout</span></span>
<span data-ttu-id="d59c1-135">Specifica il timeout del probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="d59c1-135">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="d59c1-136">Questo cmdlet contrassegna la sonda come non riuscita se non viene ricevuta una risposta valida con questo periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="d59c1-136">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="d59c1-137">I valori validi sono compresi tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="d59c1-137">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="d59c1-138">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="d59c1-138">-UnhealthyThreshold</span></span>
<span data-ttu-id="d59c1-139">Specifica il numero di tentativi di probe.</span><span class="sxs-lookup"><span data-stu-id="d59c1-139">Specifies the probe retry count.</span></span>
<span data-ttu-id="d59c1-140">Il server back-end viene contrassegnato in basso dopo il conteggio errori consecutivi Probe raggiunge la soglia non sana.</span><span class="sxs-lookup"><span data-stu-id="d59c1-140">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="d59c1-141">I valori validi sono compresi tra 1 secondo e 20 secondi.</span><span class="sxs-lookup"><span data-stu-id="d59c1-141">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="d59c1-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d59c1-142">-DefaultProfile</span></span>
<span data-ttu-id="d59c1-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d59c1-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d59c1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59c1-144">CommonParameters</span></span>
<span data-ttu-id="d59c1-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d59c1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59c1-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d59c1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59c1-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d59c1-147">INPUTS</span></span>

## <span data-ttu-id="d59c1-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d59c1-148">OUTPUTS</span></span>

### <span data-ttu-id="d59c1-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="d59c1-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="d59c1-150">Note</span><span class="sxs-lookup"><span data-stu-id="d59c1-150">NOTES</span></span>

## <span data-ttu-id="d59c1-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d59c1-151">RELATED LINKS</span></span>

[<span data-ttu-id="d59c1-152">Creare una Probe personalizzata per il gateway applicazione usando PowerShell per gestione risorse di Azure</span><span class="sxs-lookup"><span data-stu-id="d59c1-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="d59c1-153">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d59c1-153">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="d59c1-154">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d59c1-154">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="d59c1-155">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d59c1-155">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="d59c1-156">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d59c1-156">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

