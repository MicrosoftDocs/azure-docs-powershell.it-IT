---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: fff1e9190edda9ca5de12da66a2a138aa481ac7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678332"
---
# <span data-ttu-id="88386-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="88386-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="88386-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88386-102">SYNOPSIS</span></span>
<span data-ttu-id="88386-103">Crea un certificato radice attendibile per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="88386-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="88386-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88386-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88386-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88386-105">DESCRIPTION</span></span>
<span data-ttu-id="88386-106">Il cmdlet **New-AzApplicationGatewayTrustedRootCertificate** crea un certificato radice attendibile per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="88386-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="88386-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88386-107">EXAMPLES</span></span>

### <span data-ttu-id="88386-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="88386-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" --CertificateFile $certFilePath
```

<span data-ttu-id="88386-109">Questo comando crea un certificato radice attendibile denominato List "TRC1" e archivia il risultato nella variabile denominata $trc.</span><span class="sxs-lookup"><span data-stu-id="88386-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="88386-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88386-110">PARAMETERS</span></span>

### <span data-ttu-id="88386-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="88386-111">-CertificateFile</span></span>
<span data-ttu-id="88386-112">Percorso del file CER certificato</span><span class="sxs-lookup"><span data-stu-id="88386-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="88386-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88386-113">-DefaultProfile</span></span>
<span data-ttu-id="88386-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88386-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88386-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="88386-115">-Name</span></span>
<span data-ttu-id="88386-116">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="88386-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="88386-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="88386-117">-Confirm</span></span>
<span data-ttu-id="88386-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88386-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88386-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88386-119">-WhatIf</span></span>
<span data-ttu-id="88386-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88386-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88386-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88386-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88386-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88386-122">CommonParameters</span></span>
<span data-ttu-id="88386-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88386-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88386-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88386-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88386-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88386-125">INPUTS</span></span>

### <span data-ttu-id="88386-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="88386-126">None</span></span>

## <span data-ttu-id="88386-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88386-127">OUTPUTS</span></span>

### <span data-ttu-id="88386-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="88386-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="88386-129">Note</span><span class="sxs-lookup"><span data-stu-id="88386-129">NOTES</span></span>

## <span data-ttu-id="88386-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88386-130">RELATED LINKS</span></span>

[<span data-ttu-id="88386-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="88386-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="88386-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="88386-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="88386-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="88386-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="88386-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="88386-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)