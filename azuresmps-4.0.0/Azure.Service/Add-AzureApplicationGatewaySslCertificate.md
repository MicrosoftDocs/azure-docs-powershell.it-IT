---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BA63476C-25CC-444D-AD2C-51BF76374FBC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76ac1f2d1ba5c64fb12bc10320efff8c34538ab8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023694"
---
# <span data-ttu-id="c65b1-101">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c65b1-101">Add-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c65b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c65b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c65b1-103">Aggiunge un certificato SSL a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c65b1-103">Adds an SSL certificate to an Application Gateway.</span></span>

## <span data-ttu-id="c65b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c65b1-104">SYNTAX</span></span>

```
Add-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String> -Password <String>
 -CertificateFile <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c65b1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c65b1-105">DESCRIPTION</span></span>
<span data-ttu-id="c65b1-106">Il cmdlet **Add-AzureApplicationGatewaySslCertificate** aggiunge un certificato SSL (Secure Sockets Layer) a un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="c65b1-106">The **Add-AzureApplicationGatewaySslCertificate** cmdlet adds a Secure Sockets Layer (SSL) certificate to an Azure Application Gateway.</span></span>

## <span data-ttu-id="c65b1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c65b1-107">EXAMPLES</span></span>

### <span data-ttu-id="c65b1-108">Esempio 1: aggiungere un certificato SSL</span><span class="sxs-lookup"><span data-stu-id="c65b1-108">Example 1: Add an SSL certificate</span></span>
```
PS C:\> Add-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13" -Password "password" -CertificateFile "c:\Certs\sslCertificate.pfx"
```

<span data-ttu-id="c65b1-109">Questo comando aggiunge un certificato SSL denominato SslCertificate13 al gateway dell'applicazione denominato ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="c65b1-109">This command adds an SSL certificate named SslCertificate13 to the Application Gateway named ApplicationGateway08.</span></span>
<span data-ttu-id="c65b1-110">Il comando specifica il percorso del file di certificato e la password per il certificato.</span><span class="sxs-lookup"><span data-stu-id="c65b1-110">The command specifies the path of the certificate file and the password for the certificate.</span></span>

## <span data-ttu-id="c65b1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c65b1-111">PARAMETERS</span></span>

### <span data-ttu-id="c65b1-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c65b1-112">-CertificateFile</span></span>
<span data-ttu-id="c65b1-113">Specifica il percorso di un file di certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="c65b1-113">Specifies the path of an SSL certificate file.</span></span>
<span data-ttu-id="c65b1-114">Questo cmdlet aggiunge il certificato nel file specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c65b1-114">This cmdlet adds the certificate in the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="c65b1-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="c65b1-115">-CertificateName</span></span>
<span data-ttu-id="c65b1-116">Specifica il nome di un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="c65b1-116">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="c65b1-117">Questo cmdlet aggiunge il certificato specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c65b1-117">This cmdlet adds the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="c65b1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c65b1-118">-Name</span></span>
<span data-ttu-id="c65b1-119">Specifica il nome del gateway dell'applicazione a cui questo cmdlet aggiunge un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="c65b1-119">Specifies the name of the Application Gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="c65b1-120">-Password</span><span class="sxs-lookup"><span data-stu-id="c65b1-120">-Password</span></span>
<span data-ttu-id="c65b1-121">Specifica la password del certificato SSL aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c65b1-121">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c65b1-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="c65b1-122">-Profile</span></span>
<span data-ttu-id="c65b1-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c65b1-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c65b1-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c65b1-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c65b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65b1-125">CommonParameters</span></span>
<span data-ttu-id="c65b1-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c65b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65b1-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c65b1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65b1-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c65b1-128">INPUTS</span></span>

### <span data-ttu-id="c65b1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c65b1-129">System.String</span></span>

## <span data-ttu-id="c65b1-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c65b1-130">OUTPUTS</span></span>

### <span data-ttu-id="c65b1-131">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c65b1-131">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="c65b1-132">Note</span><span class="sxs-lookup"><span data-stu-id="c65b1-132">NOTES</span></span>

## <span data-ttu-id="c65b1-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c65b1-133">RELATED LINKS</span></span>

[<span data-ttu-id="c65b1-134">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c65b1-134">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c65b1-135">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c65b1-135">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
