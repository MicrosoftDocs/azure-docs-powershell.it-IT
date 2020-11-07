---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: cec5a6aa0b61889e7923ebce67d1247f99d215e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687728"
---
# <span data-ttu-id="ce609-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ce609-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="ce609-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce609-102">SYNOPSIS</span></span>
<span data-ttu-id="ce609-103">Imposta lo stato obiettivo di un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="ce609-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce609-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce609-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce609-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce609-105">DESCRIPTION</span></span>
<span data-ttu-id="ce609-106">Il cmdlet **set-AzureRmApplicationGatewaySslCertificate** imposta lo stato obiettivo di un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="ce609-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="ce609-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce609-107">EXAMPLES</span></span>

### <span data-ttu-id="ce609-108">Esempio 1: impostare lo stato dell'obiettivo di un certificato SSL</span><span class="sxs-lookup"><span data-stu-id="ce609-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="ce609-109">Questo comando imposta lo stato dell'obiettivo di un certificato SSL dal gateway dell'applicazione denominato ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="ce609-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="ce609-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce609-110">PARAMETERS</span></span>

### <span data-ttu-id="ce609-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce609-111">-ApplicationGateway</span></span>
<span data-ttu-id="ce609-112">Specifica il gateway dell'applicazione a cui è associato il certificato SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="ce609-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="ce609-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ce609-113">-CertificateFile</span></span>
<span data-ttu-id="ce609-114">Specifica il percorso del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="ce609-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="ce609-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce609-115">-Name</span></span>
<span data-ttu-id="ce609-116">Specifica il nome del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="ce609-116">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="ce609-117">-Password</span><span class="sxs-lookup"><span data-stu-id="ce609-117">-Password</span></span>
<span data-ttu-id="ce609-118">Specifica la password del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="ce609-118">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="ce609-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce609-119">-DefaultProfile</span></span>
<span data-ttu-id="ce609-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce609-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce609-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce609-121">CommonParameters</span></span>
<span data-ttu-id="ce609-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce609-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce609-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce609-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce609-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce609-124">INPUTS</span></span>

### <span data-ttu-id="ce609-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ce609-125">System.String</span></span>

## <span data-ttu-id="ce609-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce609-126">OUTPUTS</span></span>

### <span data-ttu-id="ce609-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce609-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ce609-128">Note</span><span class="sxs-lookup"><span data-stu-id="ce609-128">NOTES</span></span>

## <span data-ttu-id="ce609-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce609-129">RELATED LINKS</span></span>

[<span data-ttu-id="ce609-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ce609-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ce609-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ce609-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ce609-132">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ce609-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ce609-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ce609-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


