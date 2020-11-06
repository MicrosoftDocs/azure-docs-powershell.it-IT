---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 56cf34fce43465594a0a8862194bb15b117dda6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508107"
---
# <span data-ttu-id="27d38-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="27d38-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="27d38-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27d38-102">SYNOPSIS</span></span>
<span data-ttu-id="27d38-103">Crea una raccolta di un'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="27d38-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27d38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27d38-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27d38-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27d38-105">DESCRIPTION</span></span>
<span data-ttu-id="27d38-106">Il cmdlet **New-AzureRmPowerBIWorkspaceCollection** crea una raccolta di un'area di lavoro di Power BI per l'abbonamento a Azure nel gruppo di risorse e nella posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="27d38-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="27d38-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27d38-107">EXAMPLES</span></span>

### <span data-ttu-id="27d38-108">Esempio 1: creare una raccolta di un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="27d38-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="27d38-109">Questo comando crea una raccolta di area di lavoro denominata WCN11 nel gruppo di risorse specificato nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="27d38-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="27d38-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27d38-110">PARAMETERS</span></span>

### <span data-ttu-id="27d38-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d38-111">-DefaultProfile</span></span>
<span data-ttu-id="27d38-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="27d38-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27d38-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="27d38-113">-Location</span></span>
<span data-ttu-id="27d38-114">Specifica la posizione di Azure in cui questo cmdlet crea una raccolta di area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="27d38-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27d38-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27d38-115">-ResourceGroupName</span></span>
<span data-ttu-id="27d38-116">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una raccolta di area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="27d38-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27d38-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="27d38-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="27d38-118">Specifica un nome per la raccolta dell'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="27d38-118">Specifies a name for the Power BI workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27d38-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27d38-119">-Confirm</span></span>
<span data-ttu-id="27d38-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27d38-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d38-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27d38-121">-WhatIf</span></span>
<span data-ttu-id="27d38-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27d38-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27d38-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27d38-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d38-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d38-124">CommonParameters</span></span>
<span data-ttu-id="27d38-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27d38-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d38-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27d38-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d38-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27d38-127">INPUTS</span></span>

### <span data-ttu-id="27d38-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="27d38-128">None</span></span>
<span data-ttu-id="27d38-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="27d38-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27d38-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27d38-130">OUTPUTS</span></span>

### <span data-ttu-id="27d38-131">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="27d38-131">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="27d38-132">Note</span><span class="sxs-lookup"><span data-stu-id="27d38-132">NOTES</span></span>

## <span data-ttu-id="27d38-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27d38-133">RELATED LINKS</span></span>

[<span data-ttu-id="27d38-134">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="27d38-134">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="27d38-135">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="27d38-135">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


