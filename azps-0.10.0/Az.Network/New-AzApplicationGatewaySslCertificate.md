---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 60d46a3d61f0799618107e9bc0727a3ff31fc337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860537"
---
# <span data-ttu-id="7efc4-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7efc4-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="7efc4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7efc4-102">SYNOPSIS</span></span>
<span data-ttu-id="7efc4-103">Crea un certificato SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="7efc4-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7efc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7efc4-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7efc4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7efc4-105">DESCRIPTION</span></span>
<span data-ttu-id="7efc4-106">Il cmdlet **New-AzApplicationGatewaySslCertificate** crea un certificato SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="7efc4-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7efc4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7efc4-107">EXAMPLES</span></span>

### <span data-ttu-id="7efc4-108">Esempio 1: creare un certificato SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="7efc4-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="7efc4-109">Questo comando crea un certificato SSL denominato Cert01 per il gateway applicazione predefinito e archivia il risultato nella variabile denominata $Cert.</span><span class="sxs-lookup"><span data-stu-id="7efc4-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="7efc4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7efc4-110">PARAMETERS</span></span>

### <span data-ttu-id="7efc4-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7efc4-111">-CertificateFile</span></span>
<span data-ttu-id="7efc4-112">Specifica il percorso del file pfx del certificato SSL creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7efc4-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7efc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efc4-113">-DefaultProfile</span></span>
<span data-ttu-id="7efc4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7efc4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7efc4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7efc4-115">-Name</span></span>
<span data-ttu-id="7efc4-116">Specifica il nome del certificato SSL creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7efc4-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7efc4-117">-Password</span><span class="sxs-lookup"><span data-stu-id="7efc4-117">-Password</span></span>
<span data-ttu-id="7efc4-118">Specifica la password del protocollo SSL creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7efc4-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7efc4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efc4-119">CommonParameters</span></span>
<span data-ttu-id="7efc4-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7efc4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7efc4-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7efc4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efc4-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7efc4-122">INPUTS</span></span>

### <span data-ttu-id="7efc4-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7efc4-123">System.String</span></span>

## <span data-ttu-id="7efc4-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7efc4-124">OUTPUTS</span></span>

### <span data-ttu-id="7efc4-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7efc4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="7efc4-126">Note</span><span class="sxs-lookup"><span data-stu-id="7efc4-126">NOTES</span></span>

## <span data-ttu-id="7efc4-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7efc4-127">RELATED LINKS</span></span>

[<span data-ttu-id="7efc4-128">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7efc4-128">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7efc4-129">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7efc4-129">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7efc4-130">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7efc4-130">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7efc4-131">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7efc4-131">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


