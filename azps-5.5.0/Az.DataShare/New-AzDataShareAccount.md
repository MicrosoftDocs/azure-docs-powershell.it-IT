---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: b24fe9e6587fe50a41d601c70c2687891bea2f16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186095"
---
# <span data-ttu-id="d24e5-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="d24e5-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="d24e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d24e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d24e5-103">Crea un nuovo account per la condivisione dei dati</span><span class="sxs-lookup"><span data-stu-id="d24e5-103">Creates new data share account</span></span>

## <span data-ttu-id="d24e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d24e5-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d24e5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d24e5-105">DESCRIPTION</span></span>
<span data-ttu-id="d24e5-106">Il cmdlet **New-AzDataShareAccount** crea un account di condivisione dati nel gruppo di risorse Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="d24e5-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="d24e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d24e5-107">EXAMPLES</span></span>

### <span data-ttu-id="d24e5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d24e5-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="d24e5-109">Crea un account denominato "WikiADS" nel gruppo di risorse "ADS"</span><span class="sxs-lookup"><span data-stu-id="d24e5-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="d24e5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d24e5-110">PARAMETERS</span></span>

### <span data-ttu-id="d24e5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d24e5-111">-AsJob</span></span>
<span data-ttu-id="d24e5-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="d24e5-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="d24e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24e5-113">-DefaultProfile</span></span>
<span data-ttu-id="d24e5-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d24e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d24e5-115">-Location</span><span class="sxs-lookup"><span data-stu-id="d24e5-115">-Location</span></span>
<span data-ttu-id="d24e5-116">Posizione in cui creare l'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="d24e5-116">The location in which to create the data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24e5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d24e5-117">-Name</span></span>
<span data-ttu-id="d24e5-118">Nome dell'account per la condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="d24e5-118">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24e5-119">-ResourceGroupName</span></span>
<span data-ttu-id="d24e5-120">Verrà creato il nome del gruppo di risorse dell'account di condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="d24e5-120">The resource group name of the azure data share account will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24e5-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="d24e5-121">-Tag</span></span>
<span data-ttu-id="d24e5-122">I tag da associare all'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="d24e5-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24e5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d24e5-123">-Confirm</span></span>
<span data-ttu-id="d24e5-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d24e5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d24e5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d24e5-125">-WhatIf</span></span>
<span data-ttu-id="d24e5-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d24e5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d24e5-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d24e5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d24e5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24e5-128">CommonParameters</span></span>
<span data-ttu-id="d24e5-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d24e5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24e5-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d24e5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24e5-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="d24e5-131">INPUTS</span></span>

### <span data-ttu-id="d24e5-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d24e5-132">None</span></span>

## <span data-ttu-id="d24e5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d24e5-133">OUTPUTS</span></span>

### <span data-ttu-id="d24e5-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="d24e5-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="d24e5-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="d24e5-135">NOTES</span></span>

## <span data-ttu-id="d24e5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d24e5-136">RELATED LINKS</span></span>
