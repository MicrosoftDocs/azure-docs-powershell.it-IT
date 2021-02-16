---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 482c289922d6b8a905bee901a34568050a52c2c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202859"
---
# <span data-ttu-id="c9b04-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c9b04-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="c9b04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9b04-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b04-103">Crea un certificato radice attendibile per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9b04-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="c9b04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9b04-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9b04-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c9b04-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b04-106">Il cmdlet **New-AzApplicationGatewayTrustedRootCertificate** crea un certificato radice attendibile per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b04-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="c9b04-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9b04-107">EXAMPLES</span></span>

### <span data-ttu-id="c9b04-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9b04-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="c9b04-109">Questo comando crea un certificato radice attendibile denominato Elenco "trc1" e archivia il risultato nella variabile $trc.</span><span class="sxs-lookup"><span data-stu-id="c9b04-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="c9b04-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9b04-110">PARAMETERS</span></span>

### <span data-ttu-id="c9b04-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c9b04-111">-CertificateFile</span></span>
<span data-ttu-id="c9b04-112">Percorso del file CER del certificato</span><span class="sxs-lookup"><span data-stu-id="c9b04-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="c9b04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b04-113">-DefaultProfile</span></span>
<span data-ttu-id="c9b04-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9b04-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c9b04-115">-Name</span></span>
<span data-ttu-id="c9b04-116">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="c9b04-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="c9b04-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9b04-117">-Confirm</span></span>
<span data-ttu-id="c9b04-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9b04-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9b04-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9b04-119">-WhatIf</span></span>
<span data-ttu-id="c9b04-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9b04-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9b04-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9b04-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9b04-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b04-122">CommonParameters</span></span>
<span data-ttu-id="c9b04-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b04-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b04-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9b04-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b04-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="c9b04-125">INPUTS</span></span>

### <span data-ttu-id="c9b04-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c9b04-126">None</span></span>

## <span data-ttu-id="c9b04-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9b04-127">OUTPUTS</span></span>

### <span data-ttu-id="c9b04-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c9b04-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="c9b04-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="c9b04-129">NOTES</span></span>

## <span data-ttu-id="c9b04-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9b04-130">RELATED LINKS</span></span>

[<span data-ttu-id="c9b04-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c9b04-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="c9b04-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c9b04-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="c9b04-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c9b04-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="c9b04-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c9b04-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
