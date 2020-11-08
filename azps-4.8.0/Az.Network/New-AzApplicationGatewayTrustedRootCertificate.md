---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 482c289922d6b8a905bee901a34568050a52c2c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192335"
---
# <span data-ttu-id="61d0a-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="61d0a-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="61d0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="61d0a-103">Crea un certificato radice attendibile per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61d0a-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="61d0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61d0a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61d0a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61d0a-105">DESCRIPTION</span></span>
<span data-ttu-id="61d0a-106">Il cmdlet **New-AzApplicationGatewayTrustedRootCertificate** crea un certificato radice attendibile per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="61d0a-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="61d0a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61d0a-107">EXAMPLES</span></span>

### <span data-ttu-id="61d0a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61d0a-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="61d0a-109">Questo comando crea un certificato radice attendibile denominato List "TRC1" e archivia il risultato nella variabile denominata $trc.</span><span class="sxs-lookup"><span data-stu-id="61d0a-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="61d0a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61d0a-110">PARAMETERS</span></span>

### <span data-ttu-id="61d0a-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="61d0a-111">-CertificateFile</span></span>
<span data-ttu-id="61d0a-112">Percorso del file CER certificato</span><span class="sxs-lookup"><span data-stu-id="61d0a-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="61d0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d0a-113">-DefaultProfile</span></span>
<span data-ttu-id="61d0a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61d0a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61d0a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="61d0a-115">-Name</span></span>
<span data-ttu-id="61d0a-116">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="61d0a-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="61d0a-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61d0a-117">-Confirm</span></span>
<span data-ttu-id="61d0a-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61d0a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61d0a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61d0a-119">-WhatIf</span></span>
<span data-ttu-id="61d0a-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61d0a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61d0a-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61d0a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61d0a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d0a-122">CommonParameters</span></span>
<span data-ttu-id="61d0a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61d0a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d0a-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61d0a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d0a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61d0a-125">INPUTS</span></span>

### <span data-ttu-id="61d0a-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="61d0a-126">None</span></span>

## <span data-ttu-id="61d0a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61d0a-127">OUTPUTS</span></span>

### <span data-ttu-id="61d0a-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="61d0a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="61d0a-129">Note</span><span class="sxs-lookup"><span data-stu-id="61d0a-129">NOTES</span></span>

## <span data-ttu-id="61d0a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61d0a-130">RELATED LINKS</span></span>

[<span data-ttu-id="61d0a-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="61d0a-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="61d0a-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="61d0a-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="61d0a-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="61d0a-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="61d0a-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="61d0a-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)