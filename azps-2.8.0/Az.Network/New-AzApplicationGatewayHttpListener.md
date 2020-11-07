---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e5593ae97692813cc36f14942edb21768517f317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853033"
---
# <span data-ttu-id="f2010-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f2010-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f2010-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2010-102">SYNOPSIS</span></span>
<span data-ttu-id="f2010-103">Crea un listener HTTP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2010-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="f2010-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2010-104">SYNTAX</span></span>

### <span data-ttu-id="f2010-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2010-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2010-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f2010-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2010-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2010-107">DESCRIPTION</span></span>
<span data-ttu-id="f2010-108">Il cmdlet **New-AzApplicationGatewayHttpListener** crea un listener HTTP per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="f2010-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="f2010-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2010-109">EXAMPLES</span></span>

### <span data-ttu-id="f2010-110">Esempio 1: creare un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="f2010-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="f2010-111">Questo comando crea un listener HTTP denominato Listener01 e archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="f2010-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="f2010-112">Esempio 2: creare un listener HTTP con SSL</span><span class="sxs-lookup"><span data-stu-id="f2010-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="f2010-113">Questo comando crea un listener HTTP che usa l'offload SSL e fornisce il certificato SSL nella variabile $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="f2010-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="f2010-114">Il comando Archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="f2010-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="f2010-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2010-115">PARAMETERS</span></span>

### <span data-ttu-id="f2010-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2010-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="f2010-117">Errore del cliente di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="f2010-117">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2010-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2010-118">-DefaultProfile</span></span>
<span data-ttu-id="f2010-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2010-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2010-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2010-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="f2010-121">Specifica l'oggetto di configurazione IP front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f2010-121">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2010-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f2010-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="f2010-123">Specifica l'ID della configurazione IP front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f2010-123">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2010-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f2010-124">-FrontendPort</span></span>
<span data-ttu-id="f2010-125">Specifica la porta front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f2010-125">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2010-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="f2010-126">-FrontendPortId</span></span>
<span data-ttu-id="f2010-127">Specifica l'ID dell'oggetto porta front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f2010-127">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2010-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="f2010-128">-HostName</span></span>
<span data-ttu-id="f2010-129">Specifica il nome host del listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2010-129">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="f2010-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2010-130">-Name</span></span>
<span data-ttu-id="f2010-131">Specifica il nome del listener HTTP creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2010-131">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f2010-132">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="f2010-132">-Protocol</span></span>
<span data-ttu-id="f2010-133">Specifica il protocollo usato dal listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f2010-133">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="f2010-134">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="f2010-134">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2010-135">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="f2010-135">-SslCertificate</span></span>
<span data-ttu-id="f2010-136">Specifica l'oggetto certificato SSL per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f2010-136">Specifies the SSL certificate object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2010-137">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="f2010-137">-SslCertificateId</span></span>
<span data-ttu-id="f2010-138">Specifica l'ID del certificato SSL per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f2010-138">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2010-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2010-139">CommonParameters</span></span>
<span data-ttu-id="f2010-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2010-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2010-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2010-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2010-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2010-142">INPUTS</span></span>

### <span data-ttu-id="f2010-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f2010-143">None</span></span>

## <span data-ttu-id="f2010-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2010-144">OUTPUTS</span></span>

### <span data-ttu-id="f2010-145">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f2010-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f2010-146">Note</span><span class="sxs-lookup"><span data-stu-id="f2010-146">NOTES</span></span>

## <span data-ttu-id="f2010-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2010-147">RELATED LINKS</span></span>

[<span data-ttu-id="f2010-148">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f2010-148">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f2010-149">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f2010-149">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f2010-150">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f2010-150">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f2010-151">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f2010-151">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


