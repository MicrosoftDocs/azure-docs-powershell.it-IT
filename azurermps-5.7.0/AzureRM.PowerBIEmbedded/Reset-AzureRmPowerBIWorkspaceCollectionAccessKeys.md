---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/reset-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 99a575d4eb17cc41eeea49f1db2a801bb6a28c98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508104"
---
# <span data-ttu-id="b82dd-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="b82dd-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="b82dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b82dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b82dd-103">Reimposta il tasto di scelta specificato.</span><span class="sxs-lookup"><span data-stu-id="b82dd-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b82dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b82dd-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b82dd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b82dd-105">DESCRIPTION</span></span>
<span data-ttu-id="b82dd-106">Il cmdlet **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** Reimposta il codice di accesso specificato nella raccolta dell'area di lavoro di Power bi.</span><span class="sxs-lookup"><span data-stu-id="b82dd-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="b82dd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b82dd-107">EXAMPLES</span></span>

### <span data-ttu-id="b82dd-108">Esempio 1: reimpostare il tasto di scelta principale</span><span class="sxs-lookup"><span data-stu-id="b82dd-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="b82dd-109">Questo comando Reimposta il codice di accesso principale per la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b82dd-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="b82dd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b82dd-110">PARAMETERS</span></span>

### <span data-ttu-id="b82dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b82dd-111">-DefaultProfile</span></span>
<span data-ttu-id="b82dd-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b82dd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b82dd-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="b82dd-113">-Key1</span></span>
<span data-ttu-id="b82dd-114">Indica che questo cmdlet Reimposta il tasto di scelta principale.</span><span class="sxs-lookup"><span data-stu-id="b82dd-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="b82dd-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="b82dd-115">-Key2</span></span>
<span data-ttu-id="b82dd-116">Indica che questo cmdlet Reimposta il tasto di scelta secondario.</span><span class="sxs-lookup"><span data-stu-id="b82dd-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="b82dd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b82dd-117">-ResourceGroupName</span></span>
<span data-ttu-id="b82dd-118">Specifica il nome del gruppo di risorse della raccolta.</span><span class="sxs-lookup"><span data-stu-id="b82dd-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="b82dd-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="b82dd-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="b82dd-120">Specifica il nome della raccolta dell'area di lavoro di Power BI in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b82dd-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b82dd-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b82dd-121">-Confirm</span></span>
<span data-ttu-id="b82dd-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b82dd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b82dd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b82dd-123">-WhatIf</span></span>
<span data-ttu-id="b82dd-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b82dd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b82dd-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b82dd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b82dd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82dd-126">CommonParameters</span></span>
<span data-ttu-id="b82dd-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b82dd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82dd-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b82dd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82dd-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b82dd-129">INPUTS</span></span>

### <span data-ttu-id="b82dd-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b82dd-130">None</span></span>
<span data-ttu-id="b82dd-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b82dd-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b82dd-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b82dd-132">OUTPUTS</span></span>

### <span data-ttu-id="b82dd-133">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b82dd-133">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="b82dd-134">Note</span><span class="sxs-lookup"><span data-stu-id="b82dd-134">NOTES</span></span>

## <span data-ttu-id="b82dd-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b82dd-135">RELATED LINKS</span></span>

[<span data-ttu-id="b82dd-136">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="b82dd-136">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


