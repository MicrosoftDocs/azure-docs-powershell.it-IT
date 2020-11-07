---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: 6d7b41ae7250a294b86333ecf2926a2eda06d3bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685526"
---
# <span data-ttu-id="02347-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="02347-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="02347-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02347-102">SYNOPSIS</span></span>
<span data-ttu-id="02347-103">Revoca un accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="02347-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02347-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02347-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02347-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02347-105">DESCRIPTION</span></span>
<span data-ttu-id="02347-106">Il cmdlet **Revoke-AzureRmSnapshotAccess** revoca un accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="02347-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="02347-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02347-107">EXAMPLES</span></span>

### <span data-ttu-id="02347-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="02347-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="02347-109">Revocare l'accesso allo snapshot denominato "Snapshot01" nel gruppo di risorse denominato "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="02347-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="02347-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02347-110">PARAMETERS</span></span>

### <span data-ttu-id="02347-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02347-111">-DefaultProfile</span></span>
<span data-ttu-id="02347-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="02347-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02347-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02347-113">-ResourceGroupName</span></span>
<span data-ttu-id="02347-114">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="02347-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="02347-115">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="02347-115">-SnapshotName</span></span>
<span data-ttu-id="02347-116">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="02347-116">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="02347-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="02347-117">-Confirm</span></span>
<span data-ttu-id="02347-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02347-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02347-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02347-119">-WhatIf</span></span>
<span data-ttu-id="02347-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02347-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02347-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02347-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02347-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02347-122">CommonParameters</span></span>
<span data-ttu-id="02347-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02347-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02347-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02347-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02347-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02347-125">INPUTS</span></span>

### <span data-ttu-id="02347-126">System. String</span><span class="sxs-lookup"><span data-stu-id="02347-126">System.String</span></span>

## <span data-ttu-id="02347-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02347-127">OUTPUTS</span></span>

### <span data-ttu-id="02347-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="02347-128">System.Object</span></span>

## <span data-ttu-id="02347-129">Note</span><span class="sxs-lookup"><span data-stu-id="02347-129">NOTES</span></span>

## <span data-ttu-id="02347-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02347-130">RELATED LINKS</span></span>

