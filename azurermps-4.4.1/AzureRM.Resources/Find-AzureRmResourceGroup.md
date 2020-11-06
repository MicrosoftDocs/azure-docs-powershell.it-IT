---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513008"
---
# <span data-ttu-id="47695-101">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="47695-101">Find-AzureRmResourceGroup</span></span>

## <span data-ttu-id="47695-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47695-102">SYNOPSIS</span></span>
<span data-ttu-id="47695-103">Cerca gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="47695-103">Searches for resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47695-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47695-104">SYNTAX</span></span>

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47695-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47695-105">DESCRIPTION</span></span>
<span data-ttu-id="47695-106">Il cmdlet **Find-AzureRmResourceGroup** Cerca i gruppi di risorse usando i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="47695-106">The **Find-AzureRmResourceGroup** cmdlet searches for resource groups using the specified parameters.</span></span>

## <span data-ttu-id="47695-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47695-107">EXAMPLES</span></span>

### <span data-ttu-id="47695-108">Esempio 1: trovare tutti i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="47695-108">Example 1: Find all resource groups</span></span>
```
PS C:\>Find-AzureRmResourceGroup
```

<span data-ttu-id="47695-109">Questo comando Trova tutti i gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="47695-109">This command finds all resource groups.</span></span>

### <span data-ttu-id="47695-110">Esempio 2: trovare i gruppi di risorse per nome di tag</span><span class="sxs-lookup"><span data-stu-id="47695-110">Example 2: Find resource groups by tag name</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

<span data-ttu-id="47695-111">Questo comando Trova tutti i gruppi di risorse con un tag denominato testtag.</span><span class="sxs-lookup"><span data-stu-id="47695-111">This command finds all resource groups that have a tag named testtag.</span></span>

### <span data-ttu-id="47695-112">Esempio 3: trovare i gruppi di risorse per nome di tag e valore</span><span class="sxs-lookup"><span data-stu-id="47695-112">Example 3: Find resource groups by tag name and value</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

<span data-ttu-id="47695-113">Questo comando Trova tutti i gruppi di risorse con un tag denominato testtag e il valore testVal.</span><span class="sxs-lookup"><span data-stu-id="47695-113">This command finds all resource groups that have a tag named testtag and the value testval.</span></span>

## <span data-ttu-id="47695-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47695-114">PARAMETERS</span></span>

### <span data-ttu-id="47695-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="47695-115">-ApiVersion</span></span>
<span data-ttu-id="47695-116">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="47695-116">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="47695-117">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="47695-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47695-118">-Pre</span><span class="sxs-lookup"><span data-stu-id="47695-118">-Pre</span></span>
<span data-ttu-id="47695-119">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="47695-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="47695-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="47695-120">-Tag</span></span>
<span data-ttu-id="47695-121">Specifica le informazioni sui tag, come tabella hash, per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="47695-121">Specifies tag information, as a hash table, to filter your results.</span></span> <span data-ttu-id="47695-122">Usare i formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="47695-122">Use the following formats:</span></span>

<span data-ttu-id="47695-123">@ {tagName = $null} o @ {tagName =' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="47695-123">@{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47695-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47695-124">-DefaultProfile</span></span>
<span data-ttu-id="47695-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47695-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47695-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47695-126">CommonParameters</span></span>
<span data-ttu-id="47695-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47695-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47695-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47695-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47695-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47695-129">INPUTS</span></span>

## <span data-ttu-id="47695-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47695-130">OUTPUTS</span></span>

### <span data-ttu-id="47695-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="47695-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="47695-132">Note</span><span class="sxs-lookup"><span data-stu-id="47695-132">NOTES</span></span>

## <span data-ttu-id="47695-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47695-133">RELATED LINKS</span></span>

