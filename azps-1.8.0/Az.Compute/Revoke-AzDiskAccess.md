---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 6fe1fee57942c72b51382b6332df22993a9bb56e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836695"
---
# <span data-ttu-id="96994-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="96994-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="96994-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96994-102">SYNOPSIS</span></span>
<span data-ttu-id="96994-103">Revoca un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="96994-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="96994-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96994-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96994-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96994-105">DESCRIPTION</span></span>
<span data-ttu-id="96994-106">Il cmdlet **Revoke-AzDiskAccess** revoca un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="96994-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="96994-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96994-107">EXAMPLES</span></span>

### <span data-ttu-id="96994-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="96994-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="96994-109">Revocare l'accesso al disco denominato "Disk01" nel gruppo di risorse denominato "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="96994-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="96994-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96994-110">PARAMETERS</span></span>

### <span data-ttu-id="96994-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96994-111">-AsJob</span></span>
<span data-ttu-id="96994-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="96994-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96994-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96994-113">-DefaultProfile</span></span>
<span data-ttu-id="96994-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96994-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96994-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="96994-115">-DiskName</span></span>
<span data-ttu-id="96994-116">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="96994-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="96994-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96994-117">-ResourceGroupName</span></span>
<span data-ttu-id="96994-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="96994-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="96994-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="96994-119">-Confirm</span></span>
<span data-ttu-id="96994-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96994-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96994-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96994-121">-WhatIf</span></span>
<span data-ttu-id="96994-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96994-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96994-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96994-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96994-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96994-124">CommonParameters</span></span>
<span data-ttu-id="96994-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96994-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96994-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96994-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96994-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96994-127">INPUTS</span></span>

### <span data-ttu-id="96994-128">System. String</span><span class="sxs-lookup"><span data-stu-id="96994-128">System.String</span></span>

## <span data-ttu-id="96994-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96994-129">OUTPUTS</span></span>

### <span data-ttu-id="96994-130">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="96994-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="96994-131">Note</span><span class="sxs-lookup"><span data-stu-id="96994-131">NOTES</span></span>

## <span data-ttu-id="96994-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96994-132">RELATED LINKS</span></span>
