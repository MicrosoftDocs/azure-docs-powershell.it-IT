---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189447"
---
# <span data-ttu-id="4f689-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f689-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="4f689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f689-102">SYNOPSIS</span></span>
<span data-ttu-id="4f689-103">Imposta i tag per un suffisso PublicIpPrefix esistente</span><span class="sxs-lookup"><span data-stu-id="4f689-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="4f689-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f689-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f689-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4f689-105">DESCRIPTION</span></span>
<span data-ttu-id="4f689-106">Il cmdlet **Set-AzPublicIpPrefix** imposta i tag per un prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="4f689-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="4f689-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f689-107">EXAMPLES</span></span>

### <span data-ttu-id="4f689-108">Impostare i tag per il prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="4f689-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="4f689-109">Il primo comando ottiene un prefisso IP pubblico esistente, il secondo imposta la proprietà Tag e il terzo comando aggiorna l'oggetto esistente.</span><span class="sxs-lookup"><span data-stu-id="4f689-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="4f689-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f689-110">PARAMETERS</span></span>

### <span data-ttu-id="4f689-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f689-111">-AsJob</span></span>
<span data-ttu-id="4f689-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4f689-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f689-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f689-113">-DefaultProfile</span></span>
<span data-ttu-id="4f689-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f689-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f689-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f689-115">-PublicIpPrefix</span></span>
<span data-ttu-id="4f689-116">Lo suffisso PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f689-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f689-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f689-117">-Confirm</span></span>
<span data-ttu-id="4f689-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f689-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f689-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f689-119">-WhatIf</span></span>
<span data-ttu-id="4f689-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f689-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f689-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f689-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f689-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f689-122">CommonParameters</span></span>
<span data-ttu-id="4f689-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f689-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f689-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f689-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f689-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="4f689-125">INPUTS</span></span>

### <span data-ttu-id="4f689-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f689-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="4f689-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f689-127">OUTPUTS</span></span>

### <span data-ttu-id="4f689-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f689-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="4f689-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="4f689-129">NOTES</span></span>

## <span data-ttu-id="4f689-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f689-130">RELATED LINKS</span></span>

[<span data-ttu-id="4f689-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f689-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="4f689-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f689-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="4f689-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4f689-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
