---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: eb71d1a74e68bdf4157cacd4b87aa9a05bdc00db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507576"
---
# <span data-ttu-id="db292-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="db292-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="db292-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db292-102">SYNOPSIS</span></span>
<span data-ttu-id="db292-103">Revoca un accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="db292-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db292-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db292-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db292-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db292-105">DESCRIPTION</span></span>
<span data-ttu-id="db292-106">Il cmdlet **Revoke-AzureRmSnapshotAccess** revoca un accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="db292-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="db292-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db292-107">EXAMPLES</span></span>

### <span data-ttu-id="db292-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db292-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="db292-109">Revocare l'accesso allo snapshot denominato "Snapshot01" nel gruppo di risorse denominato "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="db292-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="db292-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db292-110">PARAMETERS</span></span>

### <span data-ttu-id="db292-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db292-111">-AsJob</span></span>
<span data-ttu-id="db292-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="db292-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db292-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db292-113">-DefaultProfile</span></span>
<span data-ttu-id="db292-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db292-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db292-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db292-115">-ResourceGroupName</span></span>
<span data-ttu-id="db292-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db292-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="db292-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="db292-117">-SnapshotName</span></span>
<span data-ttu-id="db292-118">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="db292-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="db292-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db292-119">-Confirm</span></span>
<span data-ttu-id="db292-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db292-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db292-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db292-121">-WhatIf</span></span>
<span data-ttu-id="db292-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db292-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db292-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db292-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db292-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db292-124">CommonParameters</span></span>
<span data-ttu-id="db292-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db292-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db292-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db292-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db292-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db292-127">INPUTS</span></span>

### <span data-ttu-id="db292-128">System. String</span><span class="sxs-lookup"><span data-stu-id="db292-128">System.String</span></span>

## <span data-ttu-id="db292-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db292-129">OUTPUTS</span></span>

### <span data-ttu-id="db292-130">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="db292-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="db292-131">Note</span><span class="sxs-lookup"><span data-stu-id="db292-131">NOTES</span></span>

## <span data-ttu-id="db292-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db292-132">RELATED LINKS</span></span>
