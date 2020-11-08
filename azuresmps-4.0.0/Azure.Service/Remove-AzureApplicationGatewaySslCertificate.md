---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 98AC0FAA-4786-4172-908E-FEB8588B0D74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da9e9af2e96ee177a91dae7b7ccd12f7e588517
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029956"
---
# <span data-ttu-id="c3cd2-101">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c3cd2-101">Remove-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c3cd2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cd2-103">Rimuove un certificato SSL da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3cd2-103">Removes an SSL certificate from an application gateway.</span></span>

## <span data-ttu-id="c3cd2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3cd2-104">SYNTAX</span></span>

```
Remove-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c3cd2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3cd2-105">DESCRIPTION</span></span>
<span data-ttu-id="c3cd2-106">Il cmdlet **Remove-AzureApplicationGatewaySslCertificate** rimuove un certificato SSL (Secure Sockets Layer) da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3cd2-106">The **Remove-AzureApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an application gateway.</span></span>

## <span data-ttu-id="c3cd2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3cd2-107">EXAMPLES</span></span>

### <span data-ttu-id="c3cd2-108">Esempio 1: rimuovere un certificato SSL</span><span class="sxs-lookup"><span data-stu-id="c3cd2-108">Example 1: Remove an SSL certificate</span></span>
```
PS C:\> Remove-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="c3cd2-109">Questo comando rimuove un certificato SSL denominato SslCertificate13 dal gateway dell'applicazione denominato ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="c3cd2-109">This command removes an SSL certificate named SslCertificate13 from the application gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="c3cd2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3cd2-110">PARAMETERS</span></span>

### <span data-ttu-id="c3cd2-111">-Certificate</span><span class="sxs-lookup"><span data-stu-id="c3cd2-111">-CertificateName</span></span>
<span data-ttu-id="c3cd2-112">Specifica il nome di un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="c3cd2-112">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="c3cd2-113">Questo cmdlet rimuove il certificato specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c3cd2-113">This cmdlet removes the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="c3cd2-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3cd2-114">-Name</span></span>
<span data-ttu-id="c3cd2-115">Specifica il nome del gateway dell'applicazione da cui questo cmdlet rimuove un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="c3cd2-115">Specifies the name of the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="c3cd2-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="c3cd2-116">-Profile</span></span>
<span data-ttu-id="c3cd2-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3cd2-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3cd2-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c3cd2-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c3cd2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cd2-119">CommonParameters</span></span>
<span data-ttu-id="c3cd2-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3cd2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cd2-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3cd2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cd2-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3cd2-122">INPUTS</span></span>

### <span data-ttu-id="c3cd2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c3cd2-123">System.String</span></span>

## <span data-ttu-id="c3cd2-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3cd2-124">OUTPUTS</span></span>

### <span data-ttu-id="c3cd2-125">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c3cd2-125">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="c3cd2-126">Note</span><span class="sxs-lookup"><span data-stu-id="c3cd2-126">NOTES</span></span>

## <span data-ttu-id="c3cd2-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3cd2-127">RELATED LINKS</span></span>

[<span data-ttu-id="c3cd2-128">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c3cd2-128">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c3cd2-129">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c3cd2-129">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)
