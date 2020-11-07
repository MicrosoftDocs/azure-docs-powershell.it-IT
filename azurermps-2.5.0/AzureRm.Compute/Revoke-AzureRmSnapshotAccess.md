---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: bbde391c56d4b50320f15441b75b93d125771ccb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867141"
---
# <span data-ttu-id="61772-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="61772-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="61772-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61772-102">SYNOPSIS</span></span>
<span data-ttu-id="61772-103">Revoca un accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="61772-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61772-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61772-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61772-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61772-105">DESCRIPTION</span></span>
<span data-ttu-id="61772-106">Il cmdlet **Revoke-AzureRmSnapshotAccess** revoca un accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="61772-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="61772-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61772-107">EXAMPLES</span></span>

### <span data-ttu-id="61772-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61772-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="61772-109">Revocare l'accesso allo snapshot denominato "Snapshot01" nel gruppo di risorse denominato "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="61772-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="61772-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61772-110">PARAMETERS</span></span>

### <span data-ttu-id="61772-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61772-111">-AsJob</span></span>
<span data-ttu-id="61772-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="61772-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61772-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61772-113">-DefaultProfile</span></span>
<span data-ttu-id="61772-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61772-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61772-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61772-115">-ResourceGroupName</span></span>
<span data-ttu-id="61772-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="61772-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="61772-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="61772-117">-SnapshotName</span></span>
<span data-ttu-id="61772-118">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="61772-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="61772-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61772-119">-Confirm</span></span>
<span data-ttu-id="61772-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61772-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61772-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61772-121">-WhatIf</span></span>
<span data-ttu-id="61772-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61772-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61772-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61772-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61772-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61772-124">CommonParameters</span></span>
<span data-ttu-id="61772-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61772-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61772-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61772-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61772-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61772-127">INPUTS</span></span>

### <span data-ttu-id="61772-128">System. String</span><span class="sxs-lookup"><span data-stu-id="61772-128">System.String</span></span>

## <span data-ttu-id="61772-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61772-129">OUTPUTS</span></span>

### <span data-ttu-id="61772-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="61772-130">System.Object</span></span>

## <span data-ttu-id="61772-131">Note</span><span class="sxs-lookup"><span data-stu-id="61772-131">NOTES</span></span>

## <span data-ttu-id="61772-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61772-132">RELATED LINKS</span></span>

