---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: 215ae1149cdfd939db242907a00b82b1e9fd82a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001757"
---
# <span data-ttu-id="94ba3-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="94ba3-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="94ba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="94ba3-103">Concede l'accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="94ba3-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="94ba3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94ba3-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94ba3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94ba3-105">DESCRIPTION</span></span>
<span data-ttu-id="94ba3-106">Il cmdlet **Grant-AzSnapshotAccess** concede l'accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="94ba3-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="94ba3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94ba3-107">EXAMPLES</span></span>

### <span data-ttu-id="94ba3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94ba3-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="94ba3-109">Concedere l'accesso "Lettura" alla snapshot denominata "Snapshot01" nel gruppo di risorse denominato "ResourceGroup01" per 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="94ba3-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="94ba3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94ba3-110">PARAMETERS</span></span>

### <span data-ttu-id="94ba3-111">-Access</span><span class="sxs-lookup"><span data-stu-id="94ba3-111">-Access</span></span>
<span data-ttu-id="94ba3-112">Specifica il livello di accesso.</span><span class="sxs-lookup"><span data-stu-id="94ba3-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ba3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94ba3-113">-AsJob</span></span>
<span data-ttu-id="94ba3-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="94ba3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94ba3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ba3-115">-DefaultProfile</span></span>
<span data-ttu-id="94ba3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94ba3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94ba3-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="94ba3-117">-DurationInSecond</span></span>
<span data-ttu-id="94ba3-118">Specifica la durata dell'accesso in secondi.</span><span class="sxs-lookup"><span data-stu-id="94ba3-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ba3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94ba3-119">-ResourceGroupName</span></span>
<span data-ttu-id="94ba3-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94ba3-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94ba3-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="94ba3-121">-SnapshotName</span></span>
<span data-ttu-id="94ba3-122">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="94ba3-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94ba3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94ba3-123">-Confirm</span></span>
<span data-ttu-id="94ba3-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94ba3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94ba3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94ba3-125">-WhatIf</span></span>
<span data-ttu-id="94ba3-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94ba3-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94ba3-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94ba3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94ba3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ba3-128">CommonParameters</span></span>
<span data-ttu-id="94ba3-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ba3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ba3-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94ba3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ba3-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="94ba3-131">INPUTS</span></span>

### <span data-ttu-id="94ba3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="94ba3-132">System.String</span></span>

## <span data-ttu-id="94ba3-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94ba3-133">OUTPUTS</span></span>

### <span data-ttu-id="94ba3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="94ba3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="94ba3-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="94ba3-135">NOTES</span></span>

## <span data-ttu-id="94ba3-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94ba3-136">RELATED LINKS</span></span>
