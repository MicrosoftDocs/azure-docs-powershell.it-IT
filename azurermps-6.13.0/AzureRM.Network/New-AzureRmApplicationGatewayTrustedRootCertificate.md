---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5f71f9a28eb1daae1bee070907675c87002241f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521837"
---
# <span data-ttu-id="0d9c6-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0d9c6-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="0d9c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="0d9c6-103">Crea un certificato radice attendibile per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d9c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d9c6-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d9c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d9c6-105">DESCRIPTION</span></span>
<span data-ttu-id="0d9c6-106">Il cmdlet **New-AzureRmApplicationGatewayTrustedRootCertificate** crea un certificato radice attendibile per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-106">The **New-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="0d9c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d9c6-107">EXAMPLES</span></span>

### <span data-ttu-id="0d9c6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d9c6-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzureRmApplicationGatewayTrustedRootCertificate -Name "trc1" --CertificateFile $certFilePath
```

<span data-ttu-id="0d9c6-109">Questo comando crea un certificato radice attendibile denominato List "TRC1" e archivia il risultato nella variabile denominata $trc.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="0d9c6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d9c6-110">PARAMETERS</span></span>

### <span data-ttu-id="0d9c6-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0d9c6-111">-CertificateFile</span></span>
<span data-ttu-id="0d9c6-112">Percorso del file CER certificato</span><span class="sxs-lookup"><span data-stu-id="0d9c6-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="0d9c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d9c6-113">-DefaultProfile</span></span>
<span data-ttu-id="0d9c6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d9c6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d9c6-115">-Name</span></span>
<span data-ttu-id="0d9c6-116">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="0d9c6-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="0d9c6-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0d9c6-117">-Confirm</span></span>
<span data-ttu-id="0d9c6-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9c6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d9c6-119">-WhatIf</span></span>
<span data-ttu-id="0d9c6-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d9c6-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9c6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d9c6-122">CommonParameters</span></span>
<span data-ttu-id="0d9c6-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d9c6-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d9c6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d9c6-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d9c6-125">INPUTS</span></span>

### <span data-ttu-id="0d9c6-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0d9c6-126">None</span></span>

## <span data-ttu-id="0d9c6-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d9c6-127">OUTPUTS</span></span>

### <span data-ttu-id="0d9c6-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0d9c6-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="0d9c6-129">Note</span><span class="sxs-lookup"><span data-stu-id="0d9c6-129">NOTES</span></span>

## <span data-ttu-id="0d9c6-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d9c6-130">RELATED LINKS</span></span>
