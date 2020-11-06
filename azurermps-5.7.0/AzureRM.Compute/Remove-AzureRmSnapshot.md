---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 36dec1f8d4374f2e5bbed1f742aa7733bb760f67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514480"
---
# <span data-ttu-id="8a3eb-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="8a3eb-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="8a3eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a3eb-102">SYNOPSIS</span></span>
<span data-ttu-id="8a3eb-103">Rimuove uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="8a3eb-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a3eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a3eb-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a3eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a3eb-105">DESCRIPTION</span></span>
<span data-ttu-id="8a3eb-106">Il cmdlet **Remove-AzureRmSnapshot** rimuove uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="8a3eb-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="8a3eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a3eb-107">EXAMPLES</span></span>

### <span data-ttu-id="8a3eb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8a3eb-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="8a3eb-109">Questo comando rimuove lo snapshot denominato "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="8a3eb-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8a3eb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a3eb-110">PARAMETERS</span></span>

### <span data-ttu-id="8a3eb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8a3eb-111">-Force</span></span>
<span data-ttu-id="8a3eb-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8a3eb-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a3eb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a3eb-113">-ResourceGroupName</span></span>
<span data-ttu-id="8a3eb-114">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8a3eb-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8a3eb-115">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="8a3eb-115">-SnapshotName</span></span>
<span data-ttu-id="8a3eb-116">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="8a3eb-116">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="8a3eb-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a3eb-117">-Confirm</span></span>
<span data-ttu-id="8a3eb-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a3eb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a3eb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a3eb-119">-WhatIf</span></span>
<span data-ttu-id="8a3eb-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a3eb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a3eb-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a3eb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a3eb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a3eb-122">CommonParameters</span></span>
<span data-ttu-id="8a3eb-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a3eb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a3eb-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a3eb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a3eb-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a3eb-125">INPUTS</span></span>

### <span data-ttu-id="8a3eb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8a3eb-126">System.String</span></span>

## <span data-ttu-id="8a3eb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a3eb-127">OUTPUTS</span></span>

### <span data-ttu-id="8a3eb-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="8a3eb-128">System.Object</span></span>

## <span data-ttu-id="8a3eb-129">Note</span><span class="sxs-lookup"><span data-stu-id="8a3eb-129">NOTES</span></span>

## <span data-ttu-id="8a3eb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a3eb-130">RELATED LINKS</span></span>

