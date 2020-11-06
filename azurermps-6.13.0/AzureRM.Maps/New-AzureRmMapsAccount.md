---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccount.md
ms.openlocfilehash: 0b8bfad1b3bb9f24c6b7c74e92f64c64d776c2d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516508"
---
# <span data-ttu-id="06ee6-101">New-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="06ee6-101">New-AzureRmMapsAccount</span></span>

## <span data-ttu-id="06ee6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="06ee6-103">Crea un account di Azure maps.</span><span class="sxs-lookup"><span data-stu-id="06ee6-103">Creates an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06ee6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06ee6-104">SYNTAX</span></span>

```
New-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06ee6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06ee6-105">DESCRIPTION</span></span>
<span data-ttu-id="06ee6-106">Il cmdlet New-AzureRmMapsAccount crea un account di mappe Azure con l'USK specificata.</span><span class="sxs-lookup"><span data-stu-id="06ee6-106">The New-AzureRmMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="06ee6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06ee6-107">EXAMPLES</span></span>

### <span data-ttu-id="06ee6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="06ee6-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="06ee6-109">Crea un nuovo account di Azure Maps denominato account nel gruppo di risorse MyResourceGroup con il SKU S0 e un tag.</span><span class="sxs-lookup"><span data-stu-id="06ee6-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="06ee6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06ee6-110">PARAMETERS</span></span>

### <span data-ttu-id="06ee6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ee6-111">-DefaultProfile</span></span>
<span data-ttu-id="06ee6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06ee6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06ee6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="06ee6-113">-Force</span></span>
<span data-ttu-id="06ee6-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="06ee6-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="06ee6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="06ee6-115">-Name</span></span>
<span data-ttu-id="06ee6-116">Nome dell'account mappe.</span><span class="sxs-lookup"><span data-stu-id="06ee6-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06ee6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06ee6-117">-ResourceGroupName</span></span>
<span data-ttu-id="06ee6-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="06ee6-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="06ee6-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="06ee6-119">-SkuName</span></span>
<span data-ttu-id="06ee6-120">Nome SKU account mappe.</span><span class="sxs-lookup"><span data-stu-id="06ee6-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06ee6-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="06ee6-121">-Tag</span></span>
<span data-ttu-id="06ee6-122">Associa i tag dell'account.</span><span class="sxs-lookup"><span data-stu-id="06ee6-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ee6-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06ee6-123">-Confirm</span></span>
<span data-ttu-id="06ee6-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06ee6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06ee6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06ee6-125">-WhatIf</span></span>
<span data-ttu-id="06ee6-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06ee6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06ee6-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06ee6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06ee6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ee6-128">CommonParameters</span></span>
<span data-ttu-id="06ee6-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06ee6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ee6-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06ee6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ee6-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06ee6-131">INPUTS</span></span>

### <span data-ttu-id="06ee6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="06ee6-132">System.String</span></span>

## <span data-ttu-id="06ee6-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06ee6-133">OUTPUTS</span></span>

### <span data-ttu-id="06ee6-134">Microsoft. Azure. Commands. maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="06ee6-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="06ee6-135">Note</span><span class="sxs-lookup"><span data-stu-id="06ee6-135">NOTES</span></span>

## <span data-ttu-id="06ee6-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06ee6-136">RELATED LINKS</span></span>
