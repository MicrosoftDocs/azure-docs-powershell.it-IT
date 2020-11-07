---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 5fe22889443d38e10cff061008c4ed2582825887
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863569"
---
# <span data-ttu-id="c0605-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="c0605-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="c0605-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0605-102">SYNOPSIS</span></span>
<span data-ttu-id="c0605-103">Rimuove uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="c0605-103">Removes a snapshot.</span></span>

## <span data-ttu-id="c0605-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0605-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0605-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0605-105">DESCRIPTION</span></span>
<span data-ttu-id="c0605-106">Il cmdlet **Remove-AzSnapshot** rimuove uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="c0605-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="c0605-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0605-107">EXAMPLES</span></span>

### <span data-ttu-id="c0605-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c0605-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="c0605-109">Questo comando rimuove lo snapshot denominato "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c0605-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c0605-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0605-110">PARAMETERS</span></span>

### <span data-ttu-id="c0605-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0605-111">-AsJob</span></span>
<span data-ttu-id="c0605-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="c0605-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0605-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0605-113">-DefaultProfile</span></span>
<span data-ttu-id="c0605-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0605-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0605-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c0605-115">-Force</span></span>
<span data-ttu-id="c0605-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c0605-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0605-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0605-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0605-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c0605-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0605-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="c0605-119">-SnapshotName</span></span>
<span data-ttu-id="c0605-120">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="c0605-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0605-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c0605-121">-Confirm</span></span>
<span data-ttu-id="c0605-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0605-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0605-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0605-123">-WhatIf</span></span>
<span data-ttu-id="c0605-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0605-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0605-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0605-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0605-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0605-126">CommonParameters</span></span>
<span data-ttu-id="c0605-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0605-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0605-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0605-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0605-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0605-129">INPUTS</span></span>

### <span data-ttu-id="c0605-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c0605-130">System.String</span></span>

## <span data-ttu-id="c0605-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0605-131">OUTPUTS</span></span>

### <span data-ttu-id="c0605-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="c0605-132">System.Object</span></span>

## <span data-ttu-id="c0605-133">Note</span><span class="sxs-lookup"><span data-stu-id="c0605-133">NOTES</span></span>

## <span data-ttu-id="c0605-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0605-134">RELATED LINKS</span></span>

