---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: b18db3b4e8448212b413dc13887ea68b35f22422
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952797"
---
# <span data-ttu-id="79b30-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="79b30-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="79b30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79b30-102">SYNOPSIS</span></span>
<span data-ttu-id="79b30-103">Revoca l'accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="79b30-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="79b30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79b30-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79b30-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79b30-105">DESCRIPTION</span></span>
<span data-ttu-id="79b30-106">Il cmdlet **Revoke-AzSnapshotAccess** revoca l'accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="79b30-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="79b30-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79b30-107">EXAMPLES</span></span>

### <span data-ttu-id="79b30-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79b30-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="79b30-109">Revocare l'accesso alla snapshot denominata 'Snapshot01' nel gruppo di risorse denominato 'ResourceGroup01'</span><span class="sxs-lookup"><span data-stu-id="79b30-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="79b30-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79b30-110">PARAMETERS</span></span>

### <span data-ttu-id="79b30-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79b30-111">-AsJob</span></span>
<span data-ttu-id="79b30-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="79b30-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79b30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b30-113">-DefaultProfile</span></span>
<span data-ttu-id="79b30-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79b30-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79b30-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b30-115">-ResourceGroupName</span></span>
<span data-ttu-id="79b30-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="79b30-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="79b30-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="79b30-117">-SnapshotName</span></span>
<span data-ttu-id="79b30-118">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="79b30-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="79b30-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79b30-119">-Confirm</span></span>
<span data-ttu-id="79b30-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79b30-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b30-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b30-121">-WhatIf</span></span>
<span data-ttu-id="79b30-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79b30-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79b30-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79b30-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b30-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b30-124">CommonParameters</span></span>
<span data-ttu-id="79b30-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b30-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b30-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79b30-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b30-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="79b30-127">INPUTS</span></span>

### <span data-ttu-id="79b30-128">System.String</span><span class="sxs-lookup"><span data-stu-id="79b30-128">System.String</span></span>

## <span data-ttu-id="79b30-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79b30-129">OUTPUTS</span></span>

### <span data-ttu-id="79b30-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="79b30-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="79b30-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="79b30-131">NOTES</span></span>

## <span data-ttu-id="79b30-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79b30-132">RELATED LINKS</span></span>
