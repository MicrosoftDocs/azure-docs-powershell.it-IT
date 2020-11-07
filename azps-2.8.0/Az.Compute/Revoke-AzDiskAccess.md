---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 13ae9cc51b5a1f29b995e9dd5c98ee1243339585
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675222"
---
# <span data-ttu-id="a3cf0-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a3cf0-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="a3cf0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3cf0-102">SYNOPSIS</span></span>
<span data-ttu-id="a3cf0-103">Revoca un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="a3cf0-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="a3cf0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3cf0-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3cf0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3cf0-105">DESCRIPTION</span></span>
<span data-ttu-id="a3cf0-106">Il cmdlet **Revoke-AzDiskAccess** revoca un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="a3cf0-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="a3cf0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3cf0-107">EXAMPLES</span></span>

### <span data-ttu-id="a3cf0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3cf0-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="a3cf0-109">Revocare l'accesso al disco denominato "Disk01" nel gruppo di risorse denominato "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="a3cf0-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="a3cf0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3cf0-110">PARAMETERS</span></span>

### <span data-ttu-id="a3cf0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3cf0-111">-AsJob</span></span>
<span data-ttu-id="a3cf0-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a3cf0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3cf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3cf0-113">-DefaultProfile</span></span>
<span data-ttu-id="a3cf0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3cf0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3cf0-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="a3cf0-115">-DiskName</span></span>
<span data-ttu-id="a3cf0-116">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="a3cf0-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="a3cf0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3cf0-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3cf0-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a3cf0-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a3cf0-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a3cf0-119">-Confirm</span></span>
<span data-ttu-id="a3cf0-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3cf0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3cf0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3cf0-121">-WhatIf</span></span>
<span data-ttu-id="a3cf0-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3cf0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3cf0-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3cf0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3cf0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3cf0-124">CommonParameters</span></span>
<span data-ttu-id="a3cf0-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3cf0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3cf0-126">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3cf0-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3cf0-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3cf0-127">INPUTS</span></span>

### <span data-ttu-id="a3cf0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a3cf0-128">System.String</span></span>

## <span data-ttu-id="a3cf0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3cf0-129">OUTPUTS</span></span>

### <span data-ttu-id="a3cf0-130">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a3cf0-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a3cf0-131">Note</span><span class="sxs-lookup"><span data-stu-id="a3cf0-131">NOTES</span></span>

## <span data-ttu-id="a3cf0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3cf0-132">RELATED LINKS</span></span>