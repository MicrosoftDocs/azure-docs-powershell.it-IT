---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: bcfba4bb002d7982f9a0fb9220fbce24e12e6ffb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521737"
---
# <span data-ttu-id="09985-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="09985-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="09985-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09985-102">SYNOPSIS</span></span>
<span data-ttu-id="09985-103">Rimuove un disco.</span><span class="sxs-lookup"><span data-stu-id="09985-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09985-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09985-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09985-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09985-105">DESCRIPTION</span></span>
<span data-ttu-id="09985-106">Il cmdlet **Remove-AzureRmDisk** rimuove un disco.</span><span class="sxs-lookup"><span data-stu-id="09985-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="09985-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09985-107">EXAMPLES</span></span>

### <span data-ttu-id="09985-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09985-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="09985-109">Questo comando rimuove il disco denominato "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="09985-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="09985-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09985-110">PARAMETERS</span></span>

### <span data-ttu-id="09985-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09985-111">-DefaultProfile</span></span>
<span data-ttu-id="09985-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09985-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09985-113">-Diskname</span><span class="sxs-lookup"><span data-stu-id="09985-113">-DiskName</span></span>
<span data-ttu-id="09985-114">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="09985-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="09985-115">-Force</span><span class="sxs-lookup"><span data-stu-id="09985-115">-Force</span></span>
<span data-ttu-id="09985-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="09985-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="09985-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09985-117">-ResourceGroupName</span></span>
<span data-ttu-id="09985-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09985-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="09985-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="09985-119">-Confirm</span></span>
<span data-ttu-id="09985-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09985-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09985-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09985-121">-WhatIf</span></span>
<span data-ttu-id="09985-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09985-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09985-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09985-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09985-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09985-124">CommonParameters</span></span>
<span data-ttu-id="09985-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09985-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09985-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09985-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09985-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09985-127">INPUTS</span></span>

### <span data-ttu-id="09985-128">System. String</span><span class="sxs-lookup"><span data-stu-id="09985-128">System.String</span></span>

## <span data-ttu-id="09985-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09985-129">OUTPUTS</span></span>

### <span data-ttu-id="09985-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="09985-130">System.Object</span></span>

## <span data-ttu-id="09985-131">Note</span><span class="sxs-lookup"><span data-stu-id="09985-131">NOTES</span></span>

## <span data-ttu-id="09985-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09985-132">RELATED LINKS</span></span>

