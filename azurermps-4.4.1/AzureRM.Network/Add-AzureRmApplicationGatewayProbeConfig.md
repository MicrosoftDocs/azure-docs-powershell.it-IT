---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 169a63248ebc499f577a635821131e0153e64433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520046"
---
# <span data-ttu-id="2d640-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d640-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="2d640-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d640-102">SYNOPSIS</span></span>
<span data-ttu-id="2d640-103">Aggiunge una sonda di integrità a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d640-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d640-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d640-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d640-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d640-105">DESCRIPTION</span></span>
<span data-ttu-id="2d640-106">Il cmdlet Add-AzureRmApplicationGatewayProbeConfig aggiunge una sonda di integrità a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d640-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="2d640-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d640-107">EXAMPLES</span></span>

### <span data-ttu-id="2d640-108">Esempio 1: aggiungere una sonda di integrità a un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="2d640-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="2d640-109">Questo comando aggiunge una sonda di integrità denominata Probe01 per il gateway dell'applicazione denominato gateway.</span><span class="sxs-lookup"><span data-stu-id="2d640-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="2d640-110">Il comando imposta anche la soglia non sana su 8 tentativi e timeout dopo 120 secondi.</span><span class="sxs-lookup"><span data-stu-id="2d640-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="2d640-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d640-111">PARAMETERS</span></span>

### <span data-ttu-id="2d640-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d640-112">-ApplicationGateway</span></span>
<span data-ttu-id="2d640-113">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge un probe.</span><span class="sxs-lookup"><span data-stu-id="2d640-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="2d640-114">-HostName</span><span class="sxs-lookup"><span data-stu-id="2d640-114">-HostName</span></span>
<span data-ttu-id="2d640-115">Specifica il nome host a cui il cmdlet invia il probe.</span><span class="sxs-lookup"><span data-stu-id="2d640-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="2d640-116">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="2d640-116">-Interval</span></span>
<span data-ttu-id="2d640-117">Specifica l'intervallo di probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="2d640-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="2d640-118">Questo è l'intervallo di tempo tra due sonde consecutive.</span><span class="sxs-lookup"><span data-stu-id="2d640-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="2d640-119">Questo valore è compreso tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="2d640-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="2d640-120">-Match</span><span class="sxs-lookup"><span data-stu-id="2d640-120">-Match</span></span>
<span data-ttu-id="2d640-121">Corpo che deve essere contenuto nella risposta di integrità.</span><span class="sxs-lookup"><span data-stu-id="2d640-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="2d640-122">Il valore predefinito è Empty</span><span class="sxs-lookup"><span data-stu-id="2d640-122">Default value is empty</span></span>

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

### <span data-ttu-id="2d640-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="2d640-123">-MinServers</span></span>
<span data-ttu-id="2d640-124">Numero minimo di server sempre contrassegnati come integri.</span><span class="sxs-lookup"><span data-stu-id="2d640-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="2d640-125">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="2d640-125">Default value is 0</span></span>

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

### <span data-ttu-id="2d640-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d640-126">-Name</span></span>
<span data-ttu-id="2d640-127">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="2d640-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="2d640-128">-Path</span><span class="sxs-lookup"><span data-stu-id="2d640-128">-Path</span></span>
<span data-ttu-id="2d640-129">Specifica il percorso relativo di probe.</span><span class="sxs-lookup"><span data-stu-id="2d640-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="2d640-130">Il percorso valido inizia con il carattere barra (/).</span><span class="sxs-lookup"><span data-stu-id="2d640-130">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="2d640-131">Il probe viene inviato a \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="2d640-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="2d640-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2d640-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="2d640-133">Se l'intestazione host deve essere selezionata dalle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="2d640-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="2d640-134">Il valore predefinito è false</span><span class="sxs-lookup"><span data-stu-id="2d640-134">Default value is false</span></span>

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

### <span data-ttu-id="2d640-135">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="2d640-135">-Protocol</span></span>
<span data-ttu-id="2d640-136">Specifica il protocollo usato per inviare Probe.</span><span class="sxs-lookup"><span data-stu-id="2d640-136">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="2d640-137">Questo cmdlet supporta solo HTTP.</span><span class="sxs-lookup"><span data-stu-id="2d640-137">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="2d640-138">-Timeout</span><span class="sxs-lookup"><span data-stu-id="2d640-138">-Timeout</span></span>
<span data-ttu-id="2d640-139">Specifica il timeout del probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="2d640-139">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="2d640-140">Questo cmdlet contrassegna la sonda come non riuscita se non viene ricevuta una risposta valida con questo periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="2d640-140">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="2d640-141">I valori validi sono compresi tra 1 secondo e 86400 secondi.</span><span class="sxs-lookup"><span data-stu-id="2d640-141">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="2d640-142">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="2d640-142">-UnhealthyThreshold</span></span>
<span data-ttu-id="2d640-143">Specifica il numero di tentativi di probe.</span><span class="sxs-lookup"><span data-stu-id="2d640-143">Specifies the probe retry count.</span></span>
<span data-ttu-id="2d640-144">Il server back-end viene contrassegnato in basso dopo il conteggio errori consecutivi Probe raggiunge la soglia non sana.</span><span class="sxs-lookup"><span data-stu-id="2d640-144">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="2d640-145">I valori validi sono compresi tra 1 secondo e 20 secondi.</span><span class="sxs-lookup"><span data-stu-id="2d640-145">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="2d640-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d640-146">-DefaultProfile</span></span>
<span data-ttu-id="2d640-147">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d640-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d640-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d640-148">CommonParameters</span></span>
<span data-ttu-id="2d640-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d640-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d640-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d640-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d640-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d640-151">INPUTS</span></span>

### <span data-ttu-id="2d640-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d640-152">PSApplicationGateway</span></span>
<span data-ttu-id="2d640-153">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2d640-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="2d640-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d640-154">OUTPUTS</span></span>

### <span data-ttu-id="2d640-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d640-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2d640-156">Note</span><span class="sxs-lookup"><span data-stu-id="2d640-156">NOTES</span></span>

## <span data-ttu-id="2d640-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d640-157">RELATED LINKS</span></span>

[<span data-ttu-id="2d640-158">Aggiungere una sonda a un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="2d640-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="2d640-159">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d640-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2d640-160">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d640-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2d640-161">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d640-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2d640-162">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d640-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

