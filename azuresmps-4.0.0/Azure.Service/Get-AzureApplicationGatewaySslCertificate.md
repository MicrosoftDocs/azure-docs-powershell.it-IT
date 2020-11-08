---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023622"
---
# <span data-ttu-id="37833-101">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="37833-101">Get-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="37833-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37833-102">SYNOPSIS</span></span>
<span data-ttu-id="37833-103">Ottiene i certificati del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37833-103">Gets Application Gateway certificates.</span></span>

## <span data-ttu-id="37833-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37833-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="37833-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37833-105">DESCRIPTION</span></span>
<span data-ttu-id="37833-106">Il cmdlet **Get-AzureApplicationGatewaySslCertificate** ottiene i certificati SSL (Secure Sockets Layer) per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="37833-106">The **Get-AzureApplicationGatewaySslCertificate** cmdlet gets Secure Sockets Layer (SSL) certificates for an Azure Application Gateway.</span></span>

## <span data-ttu-id="37833-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37833-107">EXAMPLES</span></span>

### <span data-ttu-id="37833-108">Esempio 1: ottenere un certificato SSL</span><span class="sxs-lookup"><span data-stu-id="37833-108">Example 1: Get an SSL certificate</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="37833-109">Questo comando ottiene un certificato SSL denominato SslCertificate13 nel gateway dell'applicazione denominato ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="37833-109">This command gets an SSL certificate named SslCertificate13 on the Application Gateway named ApplicationGateway08.</span></span>

### <span data-ttu-id="37833-110">Esempio 2: ottenere tutti i certificati SSL</span><span class="sxs-lookup"><span data-stu-id="37833-110">Example 2: Get all SSL certificates</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

<span data-ttu-id="37833-111">Questo comando consente di ottenere tutti i certificati SSL nel gateway dell'applicazione denominato ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="37833-111">This command gets all the SSL certificates on the Application Gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="37833-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37833-112">PARAMETERS</span></span>

### <span data-ttu-id="37833-113">-Certificate</span><span class="sxs-lookup"><span data-stu-id="37833-113">-CertificateName</span></span>
<span data-ttu-id="37833-114">Specifica il nome di un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="37833-114">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="37833-115">Questo cmdlet ottiene il certificato specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="37833-115">This cmdlet gets the certificate that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37833-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="37833-116">-Name</span></span>
<span data-ttu-id="37833-117">Specifica il nome del gateway dell'applicazione da cui questo cmdlet ottiene un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="37833-117">Specifies the name of the Application Gateway from which this cmdlet gets an SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37833-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="37833-118">-Profile</span></span>
<span data-ttu-id="37833-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37833-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="37833-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="37833-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37833-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37833-121">CommonParameters</span></span>
<span data-ttu-id="37833-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37833-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37833-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37833-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37833-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37833-124">INPUTS</span></span>

### <span data-ttu-id="37833-125">System. String</span><span class="sxs-lookup"><span data-stu-id="37833-125">System.String</span></span>

## <span data-ttu-id="37833-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37833-126">OUTPUTS</span></span>

### <span data-ttu-id="37833-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate, elenco<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate></span><span class="sxs-lookup"><span data-stu-id="37833-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate, List<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate></span></span>

## <span data-ttu-id="37833-128">Note</span><span class="sxs-lookup"><span data-stu-id="37833-128">NOTES</span></span>

## <span data-ttu-id="37833-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37833-129">RELATED LINKS</span></span>

[<span data-ttu-id="37833-130">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="37833-130">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="37833-131">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="37833-131">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
