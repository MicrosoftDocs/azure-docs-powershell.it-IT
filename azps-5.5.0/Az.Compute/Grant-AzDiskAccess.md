---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 39565aa0675a0afc5f6f3996cad522b435a1a9b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210059"
---
# <span data-ttu-id="b81b4-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b81b4-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="b81b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b81b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b81b4-103">Concede l'accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="b81b4-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="b81b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b81b4-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b81b4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b81b4-105">DESCRIPTION</span></span>
<span data-ttu-id="b81b4-106">Il cmdlet **Grant-AzDiskAccess** concede l'accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="b81b4-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="b81b4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b81b4-107">EXAMPLES</span></span>

### <span data-ttu-id="b81b4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b81b4-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="b81b4-109">Concedere l'accesso "Lettura" al disco denominato "Disco01" nel gruppo di risorse denominato "ResourceGroup01" per 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="b81b4-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="b81b4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b81b4-110">PARAMETERS</span></span>

### <span data-ttu-id="b81b4-111">-Access</span><span class="sxs-lookup"><span data-stu-id="b81b4-111">-Access</span></span>
<span data-ttu-id="b81b4-112">Specifica il livello di accesso.</span><span class="sxs-lookup"><span data-stu-id="b81b4-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="b81b4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b81b4-113">-AsJob</span></span>
<span data-ttu-id="b81b4-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b81b4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b81b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b81b4-115">-DefaultProfile</span></span>
<span data-ttu-id="b81b4-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b81b4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b81b4-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="b81b4-117">-DiskName</span></span>
<span data-ttu-id="b81b4-118">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="b81b4-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="b81b4-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="b81b4-119">-DurationInSecond</span></span>
<span data-ttu-id="b81b4-120">Specifica la durata dell'accesso in secondi.</span><span class="sxs-lookup"><span data-stu-id="b81b4-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="b81b4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b81b4-121">-ResourceGroupName</span></span>
<span data-ttu-id="b81b4-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b81b4-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b81b4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b81b4-123">-Confirm</span></span>
<span data-ttu-id="b81b4-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b81b4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b81b4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b81b4-125">-WhatIf</span></span>
<span data-ttu-id="b81b4-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b81b4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b81b4-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b81b4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b81b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b81b4-128">CommonParameters</span></span>
<span data-ttu-id="b81b4-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b81b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b81b4-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b81b4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b81b4-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="b81b4-131">INPUTS</span></span>

### <span data-ttu-id="b81b4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b81b4-132">System.String</span></span>

## <span data-ttu-id="b81b4-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b81b4-133">OUTPUTS</span></span>

### <span data-ttu-id="b81b4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="b81b4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="b81b4-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="b81b4-135">NOTES</span></span>

## <span data-ttu-id="b81b4-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b81b4-136">RELATED LINKS</span></span>
