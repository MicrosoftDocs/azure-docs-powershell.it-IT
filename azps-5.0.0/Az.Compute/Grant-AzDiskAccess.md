---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 39565aa0675a0afc5f6f3996cad522b435a1a9b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200270"
---
# <span data-ttu-id="f8c22-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f8c22-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="f8c22-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8c22-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c22-103">Concede un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="f8c22-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="f8c22-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8c22-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8c22-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8c22-105">DESCRIPTION</span></span>
<span data-ttu-id="f8c22-106">Il cmdlet **Grant-AzDiskAccess** concede un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="f8c22-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="f8c22-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8c22-107">EXAMPLES</span></span>

### <span data-ttu-id="f8c22-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f8c22-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="f8c22-109">Concedere l'accesso "Leggi" al disco denominato "Disk01" nel gruppo risorse denominato "ResourceGroup01" per 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="f8c22-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="f8c22-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8c22-110">PARAMETERS</span></span>

### <span data-ttu-id="f8c22-111">-Access</span><span class="sxs-lookup"><span data-stu-id="f8c22-111">-Access</span></span>
<span data-ttu-id="f8c22-112">Specifica il livello di accesso.</span><span class="sxs-lookup"><span data-stu-id="f8c22-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="f8c22-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8c22-113">-AsJob</span></span>
<span data-ttu-id="f8c22-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f8c22-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8c22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c22-115">-DefaultProfile</span></span>
<span data-ttu-id="f8c22-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c22-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8c22-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="f8c22-117">-DiskName</span></span>
<span data-ttu-id="f8c22-118">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="f8c22-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="f8c22-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="f8c22-119">-DurationInSecond</span></span>
<span data-ttu-id="f8c22-120">Specifica la durata di accesso in secondi.</span><span class="sxs-lookup"><span data-stu-id="f8c22-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="f8c22-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c22-121">-ResourceGroupName</span></span>
<span data-ttu-id="f8c22-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f8c22-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f8c22-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f8c22-123">-Confirm</span></span>
<span data-ttu-id="f8c22-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8c22-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8c22-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8c22-125">-WhatIf</span></span>
<span data-ttu-id="f8c22-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8c22-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8c22-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8c22-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8c22-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c22-128">CommonParameters</span></span>
<span data-ttu-id="f8c22-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8c22-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c22-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8c22-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c22-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8c22-131">INPUTS</span></span>

### <span data-ttu-id="f8c22-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f8c22-132">System.String</span></span>

## <span data-ttu-id="f8c22-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8c22-133">OUTPUTS</span></span>

### <span data-ttu-id="f8c22-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="f8c22-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="f8c22-135">Note</span><span class="sxs-lookup"><span data-stu-id="f8c22-135">NOTES</span></span>

## <span data-ttu-id="f8c22-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8c22-136">RELATED LINKS</span></span>