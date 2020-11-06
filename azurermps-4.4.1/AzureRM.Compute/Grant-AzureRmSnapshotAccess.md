---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 9b870214362c6e2bcd7225ef5a40ed5ff780139a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516271"
---
# <span data-ttu-id="021a5-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="021a5-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="021a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="021a5-102">SYNOPSIS</span></span>
<span data-ttu-id="021a5-103">Concede un accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="021a5-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="021a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="021a5-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="021a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="021a5-105">DESCRIPTION</span></span>
<span data-ttu-id="021a5-106">Il cmdlet **Grant-AzureRmSnapshotAccess** concede un accesso a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="021a5-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="021a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="021a5-107">EXAMPLES</span></span>

### <span data-ttu-id="021a5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="021a5-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="021a5-109">Concedere l'accesso "Leggi" allo snapshot denominato "Snapshot01" nel gruppo di risorse denominato "ResourceGroup01" per 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="021a5-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="021a5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="021a5-110">PARAMETERS</span></span>

### <span data-ttu-id="021a5-111">-Access</span><span class="sxs-lookup"><span data-stu-id="021a5-111">-Access</span></span>
<span data-ttu-id="021a5-112">Specifica il livello di accesso.</span><span class="sxs-lookup"><span data-stu-id="021a5-112">Specifies Access level.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="021a5-113">-DefaultProfile</span></span>
<span data-ttu-id="021a5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="021a5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="021a5-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="021a5-115">-DurationInSecond</span></span>
<span data-ttu-id="021a5-116">Specifica la durata di accesso in secondi.</span><span class="sxs-lookup"><span data-stu-id="021a5-116">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021a5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="021a5-117">-ResourceGroupName</span></span>
<span data-ttu-id="021a5-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="021a5-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="021a5-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="021a5-119">-SnapshotName</span></span>
<span data-ttu-id="021a5-120">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="021a5-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="021a5-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="021a5-121">-Confirm</span></span>
<span data-ttu-id="021a5-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="021a5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="021a5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="021a5-123">-WhatIf</span></span>
<span data-ttu-id="021a5-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="021a5-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="021a5-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="021a5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="021a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021a5-126">CommonParameters</span></span>
<span data-ttu-id="021a5-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="021a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021a5-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="021a5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021a5-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="021a5-129">INPUTS</span></span>

### <span data-ttu-id="021a5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="021a5-130">System.String</span></span>

## <span data-ttu-id="021a5-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="021a5-131">OUTPUTS</span></span>

### <span data-ttu-id="021a5-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="021a5-132">System.Object</span></span>

## <span data-ttu-id="021a5-133">Note</span><span class="sxs-lookup"><span data-stu-id="021a5-133">NOTES</span></span>

## <span data-ttu-id="021a5-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="021a5-134">RELATED LINKS</span></span>

