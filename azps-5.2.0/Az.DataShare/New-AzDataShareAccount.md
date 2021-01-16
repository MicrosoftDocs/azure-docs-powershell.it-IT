---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: b24fe9e6587fe50a41d601c70c2687891bea2f16
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351955"
---
# <span data-ttu-id="c1a83-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="c1a83-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="c1a83-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1a83-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a83-103">Crea un nuovo account di condivisione dati</span><span class="sxs-lookup"><span data-stu-id="c1a83-103">Creates new data share account</span></span>

## <span data-ttu-id="c1a83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1a83-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1a83-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1a83-105">DESCRIPTION</span></span>
<span data-ttu-id="c1a83-106">Cmdlet **New-AzDataShareAccount** crea un account DataShare nel gruppo di risorse Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="c1a83-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="c1a83-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1a83-107">EXAMPLES</span></span>

### <span data-ttu-id="c1a83-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1a83-108">Example 1</span></span>
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

<span data-ttu-id="c1a83-109">Crea un account denominato "WikiADS" nel gruppo risorse "annunci"</span><span class="sxs-lookup"><span data-stu-id="c1a83-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="c1a83-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1a83-110">PARAMETERS</span></span>

### <span data-ttu-id="c1a83-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1a83-111">-AsJob</span></span>
<span data-ttu-id="c1a83-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="c1a83-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="c1a83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a83-113">-DefaultProfile</span></span>
<span data-ttu-id="c1a83-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a83-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1a83-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c1a83-115">-Location</span></span>
<span data-ttu-id="c1a83-116">Posizione in cui creare l'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="c1a83-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="c1a83-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1a83-117">-Name</span></span>
<span data-ttu-id="c1a83-118">Nome dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a83-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="c1a83-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a83-119">-ResourceGroupName</span></span>
<span data-ttu-id="c1a83-120">Verrà creato il nome del gruppo di risorse dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a83-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="c1a83-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1a83-121">-Tag</span></span>
<span data-ttu-id="c1a83-122">Tag da associare all'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a83-122">The tags to associate with the azure data share account.</span></span>

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

### <span data-ttu-id="c1a83-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c1a83-123">-Confirm</span></span>
<span data-ttu-id="c1a83-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1a83-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1a83-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1a83-125">-WhatIf</span></span>
<span data-ttu-id="c1a83-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1a83-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1a83-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1a83-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1a83-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a83-128">CommonParameters</span></span>
<span data-ttu-id="c1a83-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1a83-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a83-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1a83-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a83-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1a83-131">INPUTS</span></span>

### <span data-ttu-id="c1a83-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c1a83-132">None</span></span>

## <span data-ttu-id="c1a83-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1a83-133">OUTPUTS</span></span>

### <span data-ttu-id="c1a83-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="c1a83-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="c1a83-135">Note</span><span class="sxs-lookup"><span data-stu-id="c1a83-135">NOTES</span></span>

## <span data-ttu-id="c1a83-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1a83-136">RELATED LINKS</span></span>
