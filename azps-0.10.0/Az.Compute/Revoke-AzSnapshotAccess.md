---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 4c22f8cf7ded27083ad6f1ddbd5994241d542c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863474"
---
# <span data-ttu-id="6cee1-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6cee1-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="6cee1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cee1-102">SYNOPSIS</span></span>
<span data-ttu-id="6cee1-103">Revoca un accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="6cee1-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="6cee1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cee1-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cee1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cee1-105">DESCRIPTION</span></span>
<span data-ttu-id="6cee1-106">Il cmdlet **Revoke-AzSnapshotAccess** revoca un accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="6cee1-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="6cee1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cee1-107">EXAMPLES</span></span>

### <span data-ttu-id="6cee1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6cee1-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="6cee1-109">Revocare l'accesso allo snapshot denominato "Snapshot01" nel gruppo di risorse denominato "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="6cee1-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="6cee1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cee1-110">PARAMETERS</span></span>

### <span data-ttu-id="6cee1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cee1-111">-AsJob</span></span>
<span data-ttu-id="6cee1-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6cee1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cee1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cee1-113">-DefaultProfile</span></span>
<span data-ttu-id="6cee1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6cee1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cee1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cee1-115">-ResourceGroupName</span></span>
<span data-ttu-id="6cee1-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6cee1-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6cee1-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="6cee1-117">-SnapshotName</span></span>
<span data-ttu-id="6cee1-118">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="6cee1-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="6cee1-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6cee1-119">-Confirm</span></span>
<span data-ttu-id="6cee1-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cee1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cee1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cee1-121">-WhatIf</span></span>
<span data-ttu-id="6cee1-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cee1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cee1-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cee1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cee1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cee1-124">CommonParameters</span></span>
<span data-ttu-id="6cee1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cee1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cee1-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cee1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cee1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cee1-127">INPUTS</span></span>

### <span data-ttu-id="6cee1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6cee1-128">System.String</span></span>

## <span data-ttu-id="6cee1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cee1-129">OUTPUTS</span></span>

### <span data-ttu-id="6cee1-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="6cee1-130">System.Object</span></span>

## <span data-ttu-id="6cee1-131">Note</span><span class="sxs-lookup"><span data-stu-id="6cee1-131">NOTES</span></span>

## <span data-ttu-id="6cee1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cee1-132">RELATED LINKS</span></span>

