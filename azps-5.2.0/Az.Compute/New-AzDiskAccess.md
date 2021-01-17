---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364934"
---
# <span data-ttu-id="228f1-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="228f1-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="228f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="228f1-102">SYNOPSIS</span></span>
<span data-ttu-id="228f1-103">Crea una risorsa di Access su disco</span><span class="sxs-lookup"><span data-stu-id="228f1-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="228f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="228f1-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="228f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="228f1-105">DESCRIPTION</span></span>
<span data-ttu-id="228f1-106">Il cmdlet **New-AzDiskAccess** crea una risorsa di Access su disco</span><span class="sxs-lookup"><span data-stu-id="228f1-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="228f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="228f1-107">EXAMPLES</span></span>

### <span data-ttu-id="228f1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="228f1-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="228f1-109">Questo comando creerà un accesso su disco con proprietà specificate.</span><span class="sxs-lookup"><span data-stu-id="228f1-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="228f1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="228f1-110">PARAMETERS</span></span>

### <span data-ttu-id="228f1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="228f1-111">-AsJob</span></span>
<span data-ttu-id="228f1-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="228f1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="228f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="228f1-113">-DefaultProfile</span></span>
<span data-ttu-id="228f1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="228f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="228f1-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="228f1-115">-Location</span></span>
<span data-ttu-id="228f1-116">Specifica la posizione.</span><span class="sxs-lookup"><span data-stu-id="228f1-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="228f1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="228f1-117">-Name</span></span>
<span data-ttu-id="228f1-118">Specifica il nome di un accesso su disco.</span><span class="sxs-lookup"><span data-stu-id="228f1-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="228f1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="228f1-119">-ResourceGroupName</span></span>
<span data-ttu-id="228f1-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="228f1-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="228f1-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="228f1-121">-Confirm</span></span>
<span data-ttu-id="228f1-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="228f1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="228f1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="228f1-123">-WhatIf</span></span>
<span data-ttu-id="228f1-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="228f1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="228f1-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="228f1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="228f1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="228f1-126">CommonParameters</span></span>
<span data-ttu-id="228f1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="228f1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="228f1-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="228f1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="228f1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="228f1-129">INPUTS</span></span>

### <span data-ttu-id="228f1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="228f1-130">System.String</span></span>

## <span data-ttu-id="228f1-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="228f1-131">OUTPUTS</span></span>

### <span data-ttu-id="228f1-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="228f1-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="228f1-133">Note</span><span class="sxs-lookup"><span data-stu-id="228f1-133">NOTES</span></span>

## <span data-ttu-id="228f1-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="228f1-134">RELATED LINKS</span></span>
