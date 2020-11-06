---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: c45a829414fd1009f97c99844705e9affab0ef30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509200"
---
# <span data-ttu-id="b2cea-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b2cea-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b2cea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2cea-102">SYNOPSIS</span></span>
<span data-ttu-id="b2cea-103">Imposta lo stato obiettivo di un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="b2cea-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2cea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2cea-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2cea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2cea-105">DESCRIPTION</span></span>
<span data-ttu-id="b2cea-106">Il cmdlet **set-AzureRmApplicationGatewaySslCertificate** imposta lo stato obiettivo di un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="b2cea-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="b2cea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2cea-107">EXAMPLES</span></span>

### <span data-ttu-id="b2cea-108">Esempio 1: impostare lo stato dell'obiettivo di un certificato SSL</span><span class="sxs-lookup"><span data-stu-id="b2cea-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="b2cea-109">Questo comando imposta lo stato dell'obiettivo di un certificato SSL dal gateway dell'applicazione denominato ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="b2cea-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="b2cea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2cea-110">PARAMETERS</span></span>

### <span data-ttu-id="b2cea-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2cea-111">-ApplicationGateway</span></span>
<span data-ttu-id="b2cea-112">Specifica il gateway dell'applicazione a cui è associato il certificato SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="b2cea-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="b2cea-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b2cea-113">-CertificateFile</span></span>
<span data-ttu-id="b2cea-114">Specifica il percorso del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="b2cea-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="b2cea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2cea-115">-DefaultProfile</span></span>
<span data-ttu-id="b2cea-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2cea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2cea-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2cea-117">-Name</span></span>
<span data-ttu-id="b2cea-118">Specifica il nome del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="b2cea-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="b2cea-119">-Password</span><span class="sxs-lookup"><span data-stu-id="b2cea-119">-Password</span></span>
<span data-ttu-id="b2cea-120">Specifica la password del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="b2cea-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="b2cea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2cea-121">CommonParameters</span></span>
<span data-ttu-id="b2cea-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2cea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2cea-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2cea-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2cea-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2cea-124">INPUTS</span></span>

### <span data-ttu-id="b2cea-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2cea-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="b2cea-126">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b2cea-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="b2cea-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2cea-127">OUTPUTS</span></span>

### <span data-ttu-id="b2cea-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2cea-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b2cea-129">Note</span><span class="sxs-lookup"><span data-stu-id="b2cea-129">NOTES</span></span>

## <span data-ttu-id="b2cea-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2cea-130">RELATED LINKS</span></span>

[<span data-ttu-id="b2cea-131">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b2cea-131">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b2cea-132">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b2cea-132">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b2cea-133">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b2cea-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b2cea-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b2cea-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


