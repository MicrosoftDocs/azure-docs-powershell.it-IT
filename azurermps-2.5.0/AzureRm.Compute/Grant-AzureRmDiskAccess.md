---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: c574b273082d3c7e840d589fe765190d99028d89
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866569"
---
# <span data-ttu-id="8aef6-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8aef6-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="8aef6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8aef6-102">SYNOPSIS</span></span>
<span data-ttu-id="8aef6-103">Concede un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="8aef6-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8aef6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8aef6-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8aef6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8aef6-105">DESCRIPTION</span></span>
<span data-ttu-id="8aef6-106">Il cmdlet **Grant-AzureRmDiskAccess** concede un accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="8aef6-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="8aef6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8aef6-107">EXAMPLES</span></span>

### <span data-ttu-id="8aef6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8aef6-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="8aef6-109">Concedere l'accesso "Leggi" al disco denominato "Disk01" nel gruppo risorse denominato "ResourceGroup01" per 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="8aef6-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="8aef6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8aef6-110">PARAMETERS</span></span>

### <span data-ttu-id="8aef6-111">-Access</span><span class="sxs-lookup"><span data-stu-id="8aef6-111">-Access</span></span>
<span data-ttu-id="8aef6-112">Specifica il livello di accesso.</span><span class="sxs-lookup"><span data-stu-id="8aef6-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aef6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8aef6-113">-AsJob</span></span>
<span data-ttu-id="8aef6-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8aef6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8aef6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aef6-115">-DefaultProfile</span></span>
<span data-ttu-id="8aef6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8aef6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8aef6-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="8aef6-117">-DiskName</span></span>
<span data-ttu-id="8aef6-118">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="8aef6-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="8aef6-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="8aef6-119">-DurationInSecond</span></span>
<span data-ttu-id="8aef6-120">Specifica la durata di accesso in secondi.</span><span class="sxs-lookup"><span data-stu-id="8aef6-120">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aef6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aef6-121">-ResourceGroupName</span></span>
<span data-ttu-id="8aef6-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8aef6-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8aef6-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8aef6-123">-Confirm</span></span>
<span data-ttu-id="8aef6-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aef6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aef6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aef6-125">-WhatIf</span></span>
<span data-ttu-id="8aef6-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8aef6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8aef6-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8aef6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aef6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aef6-128">CommonParameters</span></span>
<span data-ttu-id="8aef6-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aef6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aef6-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8aef6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aef6-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8aef6-131">INPUTS</span></span>

### <span data-ttu-id="8aef6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8aef6-132">System.String</span></span>

## <span data-ttu-id="8aef6-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8aef6-133">OUTPUTS</span></span>

### <span data-ttu-id="8aef6-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="8aef6-134">System.Object</span></span>

## <span data-ttu-id="8aef6-135">Note</span><span class="sxs-lookup"><span data-stu-id="8aef6-135">NOTES</span></span>

## <span data-ttu-id="8aef6-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8aef6-136">RELATED LINKS</span></span>

