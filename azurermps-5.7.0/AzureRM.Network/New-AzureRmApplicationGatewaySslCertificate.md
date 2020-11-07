---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7e75a74b99cc6a7e3da6a5f2ae2a2c3280efbfbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687899"
---
# <span data-ttu-id="15288-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="15288-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="15288-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15288-102">SYNOPSIS</span></span>
<span data-ttu-id="15288-103">Crea un certificato SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="15288-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15288-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15288-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15288-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15288-105">DESCRIPTION</span></span>
<span data-ttu-id="15288-106">Il cmdlet **New-AzureRmApplicationGatewaySslCertificate** crea un certificato SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="15288-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="15288-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15288-107">EXAMPLES</span></span>

### <span data-ttu-id="15288-108">Esempio 1: creare un certificato SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="15288-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="15288-109">Questo comando crea un certificato SSL denominato Cert01 per il gateway applicazione predefinito e archivia il risultato nella variabile denominata $Cert.</span><span class="sxs-lookup"><span data-stu-id="15288-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="15288-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15288-110">PARAMETERS</span></span>

### <span data-ttu-id="15288-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="15288-111">-CertificateFile</span></span>
<span data-ttu-id="15288-112">Specifica il percorso del file pfx del certificato SSL creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15288-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="15288-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15288-113">-DefaultProfile</span></span>
<span data-ttu-id="15288-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15288-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15288-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="15288-115">-Name</span></span>
<span data-ttu-id="15288-116">Specifica il nome del certificato SSL creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15288-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="15288-117">-Password</span><span class="sxs-lookup"><span data-stu-id="15288-117">-Password</span></span>
<span data-ttu-id="15288-118">Specifica la password del protocollo SSL creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15288-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="15288-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15288-119">CommonParameters</span></span>
<span data-ttu-id="15288-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15288-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15288-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15288-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15288-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15288-122">INPUTS</span></span>

### <span data-ttu-id="15288-123">System. String</span><span class="sxs-lookup"><span data-stu-id="15288-123">System.String</span></span>

## <span data-ttu-id="15288-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15288-124">OUTPUTS</span></span>

### <span data-ttu-id="15288-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="15288-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="15288-126">Note</span><span class="sxs-lookup"><span data-stu-id="15288-126">NOTES</span></span>

## <span data-ttu-id="15288-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15288-127">RELATED LINKS</span></span>

[<span data-ttu-id="15288-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="15288-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="15288-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="15288-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="15288-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="15288-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="15288-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="15288-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


