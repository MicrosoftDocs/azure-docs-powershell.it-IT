---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980893"
---
# <span data-ttu-id="8697c-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8697c-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="8697c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8697c-102">SYNOPSIS</span></span>
<span data-ttu-id="8697c-103">Crea una risorsa Di accesso al disco</span><span class="sxs-lookup"><span data-stu-id="8697c-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="8697c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8697c-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8697c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8697c-105">DESCRIPTION</span></span>
<span data-ttu-id="8697c-106">Il cmdlet **New-AzDiskAccess** crea una risorsa di accesso al disco</span><span class="sxs-lookup"><span data-stu-id="8697c-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="8697c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8697c-107">EXAMPLES</span></span>

### <span data-ttu-id="8697c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8697c-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="8697c-109">Questo comando crea un accesso al disco con date proprietà.</span><span class="sxs-lookup"><span data-stu-id="8697c-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="8697c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8697c-110">PARAMETERS</span></span>

### <span data-ttu-id="8697c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8697c-111">-AsJob</span></span>
<span data-ttu-id="8697c-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8697c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8697c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8697c-113">-DefaultProfile</span></span>
<span data-ttu-id="8697c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8697c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8697c-115">-Location</span><span class="sxs-lookup"><span data-stu-id="8697c-115">-Location</span></span>
<span data-ttu-id="8697c-116">Specifica la posizione.</span><span class="sxs-lookup"><span data-stu-id="8697c-116">Specifies the location.</span></span>

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

### <span data-ttu-id="8697c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8697c-117">-Name</span></span>
<span data-ttu-id="8697c-118">Specifica il nome di un accesso al disco.</span><span class="sxs-lookup"><span data-stu-id="8697c-118">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="8697c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8697c-119">-ResourceGroupName</span></span>
<span data-ttu-id="8697c-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8697c-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8697c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8697c-121">-Confirm</span></span>
<span data-ttu-id="8697c-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8697c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8697c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8697c-123">-WhatIf</span></span>
<span data-ttu-id="8697c-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8697c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8697c-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8697c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8697c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8697c-126">CommonParameters</span></span>
<span data-ttu-id="8697c-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8697c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8697c-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8697c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8697c-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="8697c-129">INPUTS</span></span>

### <span data-ttu-id="8697c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8697c-130">System.String</span></span>

## <span data-ttu-id="8697c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8697c-131">OUTPUTS</span></span>

### <span data-ttu-id="8697c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8697c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="8697c-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="8697c-133">NOTES</span></span>

## <span data-ttu-id="8697c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8697c-134">RELATED LINKS</span></span>
