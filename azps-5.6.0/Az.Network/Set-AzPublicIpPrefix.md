---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 2937aafbcffd2444051b9bed0a764cb3aede6c52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001053"
---
# <span data-ttu-id="fa92f-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fa92f-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="fa92f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa92f-102">SYNOPSIS</span></span>
<span data-ttu-id="fa92f-103">Imposta i tag per un suffisso PublicIpPrefix esistente</span><span class="sxs-lookup"><span data-stu-id="fa92f-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="fa92f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa92f-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa92f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fa92f-105">DESCRIPTION</span></span>
<span data-ttu-id="fa92f-106">Il cmdlet **Set-AzPublicIpPrefix** imposta i tag per un prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="fa92f-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="fa92f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa92f-107">EXAMPLES</span></span>

### <span data-ttu-id="fa92f-108">Impostare i tag per il prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="fa92f-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="fa92f-109">Il primo comando ottiene un prefisso IP pubblico esistente, il secondo imposta la proprietà Tag e il terzo comando aggiorna l'oggetto esistente.</span><span class="sxs-lookup"><span data-stu-id="fa92f-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="fa92f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa92f-110">PARAMETERS</span></span>

### <span data-ttu-id="fa92f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa92f-111">-AsJob</span></span>
<span data-ttu-id="fa92f-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fa92f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa92f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa92f-113">-DefaultProfile</span></span>
<span data-ttu-id="fa92f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa92f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa92f-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fa92f-115">-PublicIpPrefix</span></span>
<span data-ttu-id="fa92f-116">Lo suffisso PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fa92f-116">The PublicIpPrefix</span></span>

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

### <span data-ttu-id="fa92f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa92f-117">-Confirm</span></span>
<span data-ttu-id="fa92f-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa92f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa92f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa92f-119">-WhatIf</span></span>
<span data-ttu-id="fa92f-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa92f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa92f-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa92f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa92f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa92f-122">CommonParameters</span></span>
<span data-ttu-id="fa92f-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa92f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa92f-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa92f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa92f-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="fa92f-125">INPUTS</span></span>

### <span data-ttu-id="fa92f-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fa92f-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="fa92f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa92f-127">OUTPUTS</span></span>

### <span data-ttu-id="fa92f-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fa92f-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="fa92f-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="fa92f-129">NOTES</span></span>

## <span data-ttu-id="fa92f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa92f-130">RELATED LINKS</span></span>

[<span data-ttu-id="fa92f-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fa92f-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="fa92f-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fa92f-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="fa92f-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fa92f-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
