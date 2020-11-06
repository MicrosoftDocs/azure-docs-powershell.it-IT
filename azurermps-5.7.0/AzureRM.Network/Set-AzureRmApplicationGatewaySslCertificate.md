---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1af7ef3b60fa296a5fb8190675393a0726d0502b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511059"
---
# <span data-ttu-id="a544f-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a544f-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="a544f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a544f-102">SYNOPSIS</span></span>
<span data-ttu-id="a544f-103">Imposta lo stato obiettivo di un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="a544f-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a544f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a544f-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a544f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a544f-105">DESCRIPTION</span></span>
<span data-ttu-id="a544f-106">Il cmdlet **set-AzureRmApplicationGatewaySslCertificate** imposta lo stato obiettivo di un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="a544f-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="a544f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a544f-107">EXAMPLES</span></span>

### <span data-ttu-id="a544f-108">Esempio 1: impostare lo stato dell'obiettivo di un certificato SSL</span><span class="sxs-lookup"><span data-stu-id="a544f-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="a544f-109">Questo comando imposta lo stato dell'obiettivo di un certificato SSL dal gateway dell'applicazione denominato ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="a544f-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="a544f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a544f-110">PARAMETERS</span></span>

### <span data-ttu-id="a544f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a544f-111">-ApplicationGateway</span></span>
<span data-ttu-id="a544f-112">Specifica il gateway dell'applicazione a cui è associato il certificato SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="a544f-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a544f-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a544f-113">-CertificateFile</span></span>
<span data-ttu-id="a544f-114">Specifica il percorso del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="a544f-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="a544f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a544f-115">-DefaultProfile</span></span>
<span data-ttu-id="a544f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a544f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a544f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a544f-117">-Name</span></span>
<span data-ttu-id="a544f-118">Specifica il nome del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="a544f-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="a544f-119">-Password</span><span class="sxs-lookup"><span data-stu-id="a544f-119">-Password</span></span>
<span data-ttu-id="a544f-120">Specifica la password del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="a544f-120">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a544f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a544f-121">CommonParameters</span></span>
<span data-ttu-id="a544f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a544f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a544f-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a544f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a544f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a544f-124">INPUTS</span></span>

### <span data-ttu-id="a544f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a544f-125">System.String</span></span>

## <span data-ttu-id="a544f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a544f-126">OUTPUTS</span></span>

### <span data-ttu-id="a544f-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a544f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a544f-128">Note</span><span class="sxs-lookup"><span data-stu-id="a544f-128">NOTES</span></span>

## <span data-ttu-id="a544f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a544f-129">RELATED LINKS</span></span>

[<span data-ttu-id="a544f-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a544f-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a544f-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a544f-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a544f-132">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a544f-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a544f-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a544f-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


