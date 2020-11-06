---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7ed4af8c6d5443c3cdc7c8ae395ecc66d0a927e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511584"
---
# <span data-ttu-id="aa999-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="aa999-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="aa999-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa999-102">SYNOPSIS</span></span>
<span data-ttu-id="aa999-103">Crea una raccolta di un'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="aa999-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa999-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa999-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa999-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa999-105">DESCRIPTION</span></span>
<span data-ttu-id="aa999-106">Il cmdlet **New-AzureRmPowerBIWorkspaceCollection** crea una raccolta di un'area di lavoro di Power BI per l'abbonamento a Azure nel gruppo di risorse e nella posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="aa999-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="aa999-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa999-107">EXAMPLES</span></span>

### <span data-ttu-id="aa999-108">Esempio 1: creare una raccolta di un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="aa999-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="aa999-109">Questo comando crea una raccolta di area di lavoro denominata WCN11 nel gruppo di risorse specificato nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="aa999-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="aa999-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa999-110">PARAMETERS</span></span>

### <span data-ttu-id="aa999-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa999-111">-DefaultProfile</span></span>
<span data-ttu-id="aa999-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="aa999-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa999-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="aa999-113">-Location</span></span>
<span data-ttu-id="aa999-114">Specifica la posizione di Azure in cui questo cmdlet crea una raccolta di area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="aa999-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa999-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa999-115">-ResourceGroupName</span></span>
<span data-ttu-id="aa999-116">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una raccolta di area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="aa999-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="aa999-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="aa999-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="aa999-118">Specifica un nome per la raccolta dell'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="aa999-118">Specifies a name for the Power BI workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa999-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa999-119">-Confirm</span></span>
<span data-ttu-id="aa999-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa999-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa999-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa999-121">-WhatIf</span></span>
<span data-ttu-id="aa999-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa999-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa999-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa999-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa999-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa999-124">CommonParameters</span></span>
<span data-ttu-id="aa999-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa999-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa999-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa999-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa999-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa999-127">INPUTS</span></span>

### <span data-ttu-id="aa999-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aa999-128">System.String</span></span>

## <span data-ttu-id="aa999-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa999-129">OUTPUTS</span></span>

### <span data-ttu-id="aa999-130">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="aa999-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="aa999-131">Note</span><span class="sxs-lookup"><span data-stu-id="aa999-131">NOTES</span></span>

## <span data-ttu-id="aa999-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa999-132">RELATED LINKS</span></span>

[<span data-ttu-id="aa999-133">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="aa999-133">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="aa999-134">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="aa999-134">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


