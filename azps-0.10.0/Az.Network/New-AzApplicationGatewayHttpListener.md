---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 104a5e022d89421ac960d699c7391db660c0dd6b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860565"
---
# <span data-ttu-id="e5239-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e5239-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="e5239-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5239-102">SYNOPSIS</span></span>
<span data-ttu-id="e5239-103">Crea un listener HTTP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5239-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="e5239-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5239-104">SYNTAX</span></span>

### <span data-ttu-id="e5239-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5239-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5239-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e5239-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5239-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5239-107">DESCRIPTION</span></span>
<span data-ttu-id="e5239-108">Il cmdlet **New-AzApplicationGatewayHttpListener** crea un listener HTTP per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="e5239-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="e5239-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5239-109">EXAMPLES</span></span>

### <span data-ttu-id="e5239-110">Esempio 1: creare un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="e5239-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="e5239-111">Questo comando crea un listener HTTP denominato Listener01 e archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="e5239-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="e5239-112">Esempio 2: creare un listener HTTP con SSL</span><span class="sxs-lookup"><span data-stu-id="e5239-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="e5239-113">Questo comando crea un listener HTTP che usa l'offload SSL e fornisce il certificato SSL nella variabile $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="e5239-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="e5239-114">Il comando Archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="e5239-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="e5239-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5239-115">PARAMETERS</span></span>

### <span data-ttu-id="e5239-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5239-116">-DefaultProfile</span></span>
<span data-ttu-id="e5239-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5239-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5239-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5239-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="e5239-119">Specifica l'oggetto di configurazione IP front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e5239-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5239-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e5239-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="e5239-121">Specifica l'ID della configurazione IP front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e5239-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5239-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="e5239-122">-FrontendPort</span></span>
<span data-ttu-id="e5239-123">Specifica la porta front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e5239-123">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5239-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="e5239-124">-FrontendPortId</span></span>
<span data-ttu-id="e5239-125">Specifica l'ID dell'oggetto porta front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e5239-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5239-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="e5239-126">-HostName</span></span>
<span data-ttu-id="e5239-127">Specifica il nome host del listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5239-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="e5239-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5239-128">-Name</span></span>
<span data-ttu-id="e5239-129">Specifica il nome del listener HTTP creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5239-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e5239-130">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="e5239-130">-Protocol</span></span>
<span data-ttu-id="e5239-131">Specifica il protocollo usato dal listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e5239-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="e5239-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="e5239-132">-RequireServerNameIndication</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5239-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5239-133">-SslCertificate</span></span>
<span data-ttu-id="e5239-134">Specifica l'oggetto certificato SSL per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e5239-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5239-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="e5239-135">-SslCertificateId</span></span>
<span data-ttu-id="e5239-136">Specifica l'ID del certificato SSL per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e5239-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5239-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5239-137">CommonParameters</span></span>
<span data-ttu-id="e5239-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5239-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5239-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5239-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5239-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5239-140">INPUTS</span></span>

### <span data-ttu-id="e5239-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e5239-141">System.String</span></span>

## <span data-ttu-id="e5239-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5239-142">OUTPUTS</span></span>

### <span data-ttu-id="e5239-143">Microsoft. Azure. Commands. Network. Models. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="e5239-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="e5239-144">Note</span><span class="sxs-lookup"><span data-stu-id="e5239-144">NOTES</span></span>

## <span data-ttu-id="e5239-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5239-145">RELATED LINKS</span></span>

[<span data-ttu-id="e5239-146">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e5239-146">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="e5239-147">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e5239-147">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="e5239-148">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e5239-148">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="e5239-149">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e5239-149">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


