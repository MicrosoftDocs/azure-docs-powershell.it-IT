---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 964e99912e4f21d48e89b725da1aa44ac32ea186
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861005"
---
# <span data-ttu-id="8247a-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8247a-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="8247a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8247a-102">SYNOPSIS</span></span>
<span data-ttu-id="8247a-103">Aggiunge un certificato SSL a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8247a-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="8247a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8247a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8247a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8247a-105">DESCRIPTION</span></span>
<span data-ttu-id="8247a-106">Il cmdlet **Add-AzApplicationGatewaySslCertificate** aggiunge un certificato SSL a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8247a-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="8247a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8247a-107">EXAMPLES</span></span>

### <span data-ttu-id="8247a-108">Esempio 1: aggiungere un certificato SSL a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8247a-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="8247a-109">Questo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 e quindi aggiunge un certificato SSL denominato Cert01.</span><span class="sxs-lookup"><span data-stu-id="8247a-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="8247a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8247a-110">PARAMETERS</span></span>

### <span data-ttu-id="8247a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8247a-111">-ApplicationGateway</span></span>
<span data-ttu-id="8247a-112">Specifica il nome del gateway dell'applicazione a cui questo cmdlet aggiunge un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="8247a-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="8247a-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8247a-113">-CertificateFile</span></span>
<span data-ttu-id="8247a-114">Specifica il file PFX di un certificato SSL aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8247a-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="8247a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8247a-115">-DefaultProfile</span></span>
<span data-ttu-id="8247a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8247a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8247a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8247a-117">-Name</span></span>
<span data-ttu-id="8247a-118">Specifica il nome del certificato SSL aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8247a-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="8247a-119">-Password</span><span class="sxs-lookup"><span data-stu-id="8247a-119">-Password</span></span>
<span data-ttu-id="8247a-120">Specifica la password del certificato SSL aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8247a-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="8247a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8247a-121">CommonParameters</span></span>
<span data-ttu-id="8247a-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8247a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8247a-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8247a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8247a-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8247a-124">INPUTS</span></span>

### <span data-ttu-id="8247a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8247a-125">System.String</span></span>

## <span data-ttu-id="8247a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8247a-126">OUTPUTS</span></span>

### <span data-ttu-id="8247a-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8247a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8247a-128">Note</span><span class="sxs-lookup"><span data-stu-id="8247a-128">NOTES</span></span>

## <span data-ttu-id="8247a-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8247a-129">RELATED LINKS</span></span>

[<span data-ttu-id="8247a-130">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8247a-130">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8247a-131">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8247a-131">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8247a-132">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8247a-132">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8247a-133">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8247a-133">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


