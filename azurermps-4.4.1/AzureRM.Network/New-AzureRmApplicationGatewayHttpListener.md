---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: ea7a140d2dca2a590a8d3bc83e946d122fb8fd31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520498"
---
# <span data-ttu-id="ef019-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ef019-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ef019-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef019-102">SYNOPSIS</span></span>
<span data-ttu-id="ef019-103">Crea un listener HTTP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ef019-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef019-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef019-104">SYNTAX</span></span>

### <span data-ttu-id="ef019-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef019-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef019-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ef019-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef019-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef019-107">DESCRIPTION</span></span>
<span data-ttu-id="ef019-108">Il cmdlet **New-AzureRmApplicationGatewayHttpListener** crea un listener HTTP per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="ef019-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="ef019-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef019-109">EXAMPLES</span></span>

### <span data-ttu-id="ef019-110">Esempio 1: creare un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="ef019-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="ef019-111">Questo comando crea un listener HTTP denominato Listener01 e archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="ef019-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="ef019-112">Esempio 2: creare un listener HTTP con SSL</span><span class="sxs-lookup"><span data-stu-id="ef019-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="ef019-113">Questo comando crea un listener HTTP che usa l'offload SSL e fornisce il certificato SSL nella variabile $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="ef019-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="ef019-114">Il comando Archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="ef019-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="ef019-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef019-115">PARAMETERS</span></span>

### <span data-ttu-id="ef019-116">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef019-116">-FrontendIPConfiguration</span></span>
<span data-ttu-id="ef019-117">Specifica l'oggetto di configurazione IP front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef019-117">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="ef019-118">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ef019-118">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="ef019-119">Specifica l'ID della configurazione IP front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef019-119">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="ef019-120">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ef019-120">-FrontendPort</span></span>
<span data-ttu-id="ef019-121">Specifica la porta front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef019-121">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="ef019-122">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="ef019-122">-FrontendPortId</span></span>
<span data-ttu-id="ef019-123">Specifica l'ID dell'oggetto porta front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef019-123">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="ef019-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="ef019-124">-HostName</span></span>
<span data-ttu-id="ef019-125">Specifica il nome host del listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ef019-125">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="ef019-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef019-126">-Name</span></span>
<span data-ttu-id="ef019-127">Specifica il nome del listener HTTP creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef019-127">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ef019-128">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="ef019-128">-Protocol</span></span>
<span data-ttu-id="ef019-129">Specifica il protocollo usato dal listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef019-129">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="ef019-130">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="ef019-130">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef019-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="ef019-131">-SslCertificate</span></span>
<span data-ttu-id="ef019-132">Specifica l'oggetto certificato SSL per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef019-132">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="ef019-133">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="ef019-133">-SslCertificateId</span></span>
<span data-ttu-id="ef019-134">Specifica l'ID del certificato SSL per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef019-134">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="ef019-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef019-135">-DefaultProfile</span></span>
<span data-ttu-id="ef019-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef019-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef019-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef019-137">CommonParameters</span></span>
<span data-ttu-id="ef019-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef019-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef019-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef019-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef019-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef019-140">INPUTS</span></span>

### <span data-ttu-id="ef019-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ef019-141">System.String</span></span>

## <span data-ttu-id="ef019-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef019-142">OUTPUTS</span></span>

### <span data-ttu-id="ef019-143">Microsoft. Azure. Commands. Network. Models. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="ef019-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="ef019-144">Note</span><span class="sxs-lookup"><span data-stu-id="ef019-144">NOTES</span></span>

## <span data-ttu-id="ef019-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef019-145">RELATED LINKS</span></span>

[<span data-ttu-id="ef019-146">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ef019-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="ef019-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ef019-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="ef019-148">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ef019-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="ef019-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ef019-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


