---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: e22760c2838cf0b4fb0597dbd45532374b604b79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865902"
---
# <span data-ttu-id="ed066-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ed066-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="ed066-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed066-102">SYNOPSIS</span></span>
<span data-ttu-id="ed066-103">Crea un certificato SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="ed066-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed066-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed066-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed066-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed066-105">DESCRIPTION</span></span>
<span data-ttu-id="ed066-106">Il cmdlet **New-AzureRmApplicationGatewaySslCertificate** crea un certificato SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="ed066-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="ed066-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed066-107">EXAMPLES</span></span>

### <span data-ttu-id="ed066-108">Esempio 1: creare un certificato SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="ed066-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="ed066-109">Questo comando crea un certificato SSL denominato Cert01 per il gateway applicazione predefinito e archivia il risultato nella variabile denominata $Cert.</span><span class="sxs-lookup"><span data-stu-id="ed066-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="ed066-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed066-110">PARAMETERS</span></span>

### <span data-ttu-id="ed066-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ed066-111">-CertificateFile</span></span>
<span data-ttu-id="ed066-112">Specifica il percorso del file pfx del certificato SSL creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed066-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ed066-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed066-113">-DefaultProfile</span></span>
<span data-ttu-id="ed066-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed066-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed066-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed066-115">-Name</span></span>
<span data-ttu-id="ed066-116">Specifica il nome del certificato SSL creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed066-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ed066-117">-Password</span><span class="sxs-lookup"><span data-stu-id="ed066-117">-Password</span></span>
<span data-ttu-id="ed066-118">Specifica la password del protocollo SSL creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed066-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ed066-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed066-119">CommonParameters</span></span>
<span data-ttu-id="ed066-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed066-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed066-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed066-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed066-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed066-122">INPUTS</span></span>

### <span data-ttu-id="ed066-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ed066-123">System.String</span></span>

## <span data-ttu-id="ed066-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed066-124">OUTPUTS</span></span>

### <span data-ttu-id="ed066-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ed066-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="ed066-126">Note</span><span class="sxs-lookup"><span data-stu-id="ed066-126">NOTES</span></span>

## <span data-ttu-id="ed066-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed066-127">RELATED LINKS</span></span>

[<span data-ttu-id="ed066-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ed066-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ed066-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ed066-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ed066-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ed066-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ed066-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ed066-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


