---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: a0b6ddf2a5796c63c3efd20b811a2040db123836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521399"
---
# <span data-ttu-id="f773d-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f773d-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="f773d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f773d-102">SYNOPSIS</span></span>
<span data-ttu-id="f773d-103">Revoca un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="f773d-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f773d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f773d-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f773d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f773d-105">DESCRIPTION</span></span>
<span data-ttu-id="f773d-106">Il cmdlet **Revoke-AzureRmDiskAccess** revoca un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="f773d-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="f773d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f773d-107">EXAMPLES</span></span>

### <span data-ttu-id="f773d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f773d-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="f773d-109">Revocare l'accesso al disco denominato "Disk01" nel gruppo di risorse denominato "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="f773d-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="f773d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f773d-110">PARAMETERS</span></span>

### <span data-ttu-id="f773d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f773d-111">-AsJob</span></span>
<span data-ttu-id="f773d-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f773d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f773d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f773d-113">-DefaultProfile</span></span>
<span data-ttu-id="f773d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f773d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f773d-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="f773d-115">-DiskName</span></span>
<span data-ttu-id="f773d-116">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="f773d-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="f773d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f773d-117">-ResourceGroupName</span></span>
<span data-ttu-id="f773d-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f773d-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f773d-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f773d-119">-Confirm</span></span>
<span data-ttu-id="f773d-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f773d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f773d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f773d-121">-WhatIf</span></span>
<span data-ttu-id="f773d-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f773d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f773d-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f773d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f773d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f773d-124">CommonParameters</span></span>
<span data-ttu-id="f773d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f773d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f773d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f773d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f773d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f773d-127">INPUTS</span></span>

### <span data-ttu-id="f773d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f773d-128">System.String</span></span>

## <span data-ttu-id="f773d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f773d-129">OUTPUTS</span></span>

### <span data-ttu-id="f773d-130">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f773d-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f773d-131">Note</span><span class="sxs-lookup"><span data-stu-id="f773d-131">NOTES</span></span>

## <span data-ttu-id="f773d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f773d-132">RELATED LINKS</span></span>
