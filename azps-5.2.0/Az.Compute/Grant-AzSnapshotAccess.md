---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: a431428c670dba7e0bfb152bde0cae22f47d8099
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334315"
---
# <span data-ttu-id="ddf4d-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ddf4d-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="ddf4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddf4d-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf4d-103">Concede un accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="ddf4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddf4d-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddf4d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddf4d-105">DESCRIPTION</span></span>
<span data-ttu-id="ddf4d-106">Il cmdlet **Grant-AzSnapshotAccess** concede un accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="ddf4d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddf4d-107">EXAMPLES</span></span>

### <span data-ttu-id="ddf4d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ddf4d-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="ddf4d-109">Concedere l'accesso "Leggi" allo snapshot denominato "Snapshot01" nel gruppo di risorse denominato "ResourceGroup01" per 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="ddf4d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddf4d-110">PARAMETERS</span></span>

### <span data-ttu-id="ddf4d-111">-Access</span><span class="sxs-lookup"><span data-stu-id="ddf4d-111">-Access</span></span>
<span data-ttu-id="ddf4d-112">Specifica il livello di accesso.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="ddf4d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddf4d-113">-AsJob</span></span>
<span data-ttu-id="ddf4d-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ddf4d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddf4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf4d-115">-DefaultProfile</span></span>
<span data-ttu-id="ddf4d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddf4d-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="ddf4d-117">-DurationInSecond</span></span>
<span data-ttu-id="ddf4d-118">Specifica la durata di accesso in secondi.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="ddf4d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf4d-119">-ResourceGroupName</span></span>
<span data-ttu-id="ddf4d-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ddf4d-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="ddf4d-121">-SnapshotName</span></span>
<span data-ttu-id="ddf4d-122">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="ddf4d-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ddf4d-123">-Confirm</span></span>
<span data-ttu-id="ddf4d-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddf4d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddf4d-125">-WhatIf</span></span>
<span data-ttu-id="ddf4d-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddf4d-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddf4d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf4d-128">CommonParameters</span></span>
<span data-ttu-id="ddf4d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf4d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf4d-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddf4d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf4d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddf4d-131">INPUTS</span></span>

### <span data-ttu-id="ddf4d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ddf4d-132">System.String</span></span>

## <span data-ttu-id="ddf4d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddf4d-133">OUTPUTS</span></span>

### <span data-ttu-id="ddf4d-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="ddf4d-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="ddf4d-135">Note</span><span class="sxs-lookup"><span data-stu-id="ddf4d-135">NOTES</span></span>

## <span data-ttu-id="ddf4d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddf4d-136">RELATED LINKS</span></span>
