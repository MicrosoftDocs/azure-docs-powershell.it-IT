---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210051"
---
# <span data-ttu-id="8f614-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8f614-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="8f614-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f614-102">SYNOPSIS</span></span>
<span data-ttu-id="8f614-103">Crea una risorsa Di accesso al disco</span><span class="sxs-lookup"><span data-stu-id="8f614-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="8f614-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f614-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f614-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8f614-105">DESCRIPTION</span></span>
<span data-ttu-id="8f614-106">Il cmdlet **New-AzDiskAccess** crea una risorsa Di accesso al disco</span><span class="sxs-lookup"><span data-stu-id="8f614-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="8f614-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f614-107">EXAMPLES</span></span>

### <span data-ttu-id="8f614-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8f614-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="8f614-109">Questo comando crea un accesso al disco con date proprietà.</span><span class="sxs-lookup"><span data-stu-id="8f614-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="8f614-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f614-110">PARAMETERS</span></span>

### <span data-ttu-id="8f614-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f614-111">-AsJob</span></span>
<span data-ttu-id="8f614-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8f614-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f614-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f614-113">-DefaultProfile</span></span>
<span data-ttu-id="8f614-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f614-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f614-115">-Location</span><span class="sxs-lookup"><span data-stu-id="8f614-115">-Location</span></span>
<span data-ttu-id="8f614-116">Specifica la posizione.</span><span class="sxs-lookup"><span data-stu-id="8f614-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f614-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8f614-117">-Name</span></span>
<span data-ttu-id="8f614-118">Specifica il nome di un accesso al disco.</span><span class="sxs-lookup"><span data-stu-id="8f614-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f614-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f614-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f614-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8f614-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8f614-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f614-121">-Confirm</span></span>
<span data-ttu-id="8f614-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f614-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f614-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f614-123">-WhatIf</span></span>
<span data-ttu-id="8f614-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f614-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f614-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f614-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f614-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f614-126">CommonParameters</span></span>
<span data-ttu-id="8f614-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f614-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f614-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8f614-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f614-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="8f614-129">INPUTS</span></span>

### <span data-ttu-id="8f614-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8f614-130">System.String</span></span>

## <span data-ttu-id="8f614-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f614-131">OUTPUTS</span></span>

### <span data-ttu-id="8f614-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8f614-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="8f614-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="8f614-133">NOTES</span></span>

## <span data-ttu-id="8f614-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f614-134">RELATED LINKS</span></span>
