---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: edd2d89cfe0488021ef62780ade80cb2b98437c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509291"
---
# <span data-ttu-id="095cc-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="095cc-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="095cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="095cc-102">SYNOPSIS</span></span>
<span data-ttu-id="095cc-103">Rimuove uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="095cc-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="095cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="095cc-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="095cc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="095cc-105">DESCRIPTION</span></span>
<span data-ttu-id="095cc-106">Il cmdlet **Remove-AzureRmSnapshot** rimuove uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="095cc-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="095cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="095cc-107">EXAMPLES</span></span>

### <span data-ttu-id="095cc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="095cc-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="095cc-109">Questo comando rimuove lo snapshot denominato "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="095cc-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="095cc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="095cc-110">PARAMETERS</span></span>

### <span data-ttu-id="095cc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="095cc-111">-AsJob</span></span>
<span data-ttu-id="095cc-112">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="095cc-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="095cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095cc-113">-DefaultProfile</span></span>
<span data-ttu-id="095cc-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="095cc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095cc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="095cc-115">-Force</span></span>
<span data-ttu-id="095cc-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="095cc-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="095cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="095cc-117">-ResourceGroupName</span></span>
<span data-ttu-id="095cc-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="095cc-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095cc-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="095cc-119">-SnapshotName</span></span>
<span data-ttu-id="095cc-120">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="095cc-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095cc-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="095cc-121">-Confirm</span></span>
<span data-ttu-id="095cc-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="095cc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="095cc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="095cc-123">-WhatIf</span></span>
<span data-ttu-id="095cc-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="095cc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="095cc-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="095cc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="095cc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095cc-126">CommonParameters</span></span>
<span data-ttu-id="095cc-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095cc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095cc-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="095cc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095cc-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="095cc-129">INPUTS</span></span>

### <span data-ttu-id="095cc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="095cc-130">System.String</span></span>

## <span data-ttu-id="095cc-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="095cc-131">OUTPUTS</span></span>

### <span data-ttu-id="095cc-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="095cc-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="095cc-133">Note</span><span class="sxs-lookup"><span data-stu-id="095cc-133">NOTES</span></span>

## <span data-ttu-id="095cc-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="095cc-134">RELATED LINKS</span></span>
