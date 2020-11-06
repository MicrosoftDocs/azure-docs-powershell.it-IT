---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: fc4457e23f50dea3d70a3af2115a93e460dc6a1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520182"
---
# <span data-ttu-id="6dfcb-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6dfcb-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="6dfcb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6dfcb-102">SYNOPSIS</span></span>
<span data-ttu-id="6dfcb-103">Aggiunge un certificato SSL a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dfcb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6dfcb-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6dfcb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6dfcb-105">DESCRIPTION</span></span>
<span data-ttu-id="6dfcb-106">Il cmdlet **Add-AzureRmApplicationGatewaySslCertificate** aggiunge un certificato SSL a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="6dfcb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6dfcb-107">EXAMPLES</span></span>

### <span data-ttu-id="6dfcb-108">Esempio 1: aggiungere un certificato SSL a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="6dfcb-109">Questo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 e quindi aggiunge un certificato SSL denominato Cert01.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="6dfcb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6dfcb-110">PARAMETERS</span></span>

### <span data-ttu-id="6dfcb-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dfcb-111">-ApplicationGateway</span></span>
<span data-ttu-id="6dfcb-112">Specifica il nome del gateway dell'applicazione a cui questo cmdlet aggiunge un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="6dfcb-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="6dfcb-113">-CertificateFile</span></span>
<span data-ttu-id="6dfcb-114">Specifica il file PFX di un certificato SSL aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="6dfcb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dfcb-115">-DefaultProfile</span></span>
<span data-ttu-id="6dfcb-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dfcb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6dfcb-117">-Name</span></span>
<span data-ttu-id="6dfcb-118">Specifica il nome del certificato SSL aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="6dfcb-119">-Password</span><span class="sxs-lookup"><span data-stu-id="6dfcb-119">-Password</span></span>
<span data-ttu-id="6dfcb-120">Specifica la password del certificato SSL aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfcb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dfcb-121">CommonParameters</span></span>
<span data-ttu-id="6dfcb-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dfcb-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dfcb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dfcb-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6dfcb-124">INPUTS</span></span>

### <span data-ttu-id="6dfcb-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dfcb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="6dfcb-126">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6dfcb-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="6dfcb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6dfcb-127">OUTPUTS</span></span>

### <span data-ttu-id="6dfcb-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dfcb-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6dfcb-129">Note</span><span class="sxs-lookup"><span data-stu-id="6dfcb-129">NOTES</span></span>

## <span data-ttu-id="6dfcb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6dfcb-130">RELATED LINKS</span></span>

[<span data-ttu-id="6dfcb-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6dfcb-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6dfcb-132">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6dfcb-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6dfcb-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6dfcb-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6dfcb-134">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6dfcb-134">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


