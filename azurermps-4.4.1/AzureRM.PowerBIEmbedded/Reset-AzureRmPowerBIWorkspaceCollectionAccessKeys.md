---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 766682df23beaa7c513ff54554a3ebd59a6d1537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521171"
---
# <span data-ttu-id="7b6f2-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="7b6f2-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="7b6f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="7b6f2-103">Reimposta il tasto di scelta specificato.</span><span class="sxs-lookup"><span data-stu-id="7b6f2-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b6f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b6f2-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b6f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b6f2-105">DESCRIPTION</span></span>
<span data-ttu-id="7b6f2-106">Il cmdlet **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** Reimposta il codice di accesso specificato nella raccolta dell'area di lavoro di Power bi.</span><span class="sxs-lookup"><span data-stu-id="7b6f2-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="7b6f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b6f2-107">EXAMPLES</span></span>

### <span data-ttu-id="7b6f2-108">Esempio 1: reimpostare il tasto di scelta principale</span><span class="sxs-lookup"><span data-stu-id="7b6f2-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="7b6f2-109">Questo comando Reimposta il codice di accesso principale per la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="7b6f2-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="7b6f2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b6f2-110">PARAMETERS</span></span>

### <span data-ttu-id="7b6f2-111">-Key1</span><span class="sxs-lookup"><span data-stu-id="7b6f2-111">-Key1</span></span>
<span data-ttu-id="7b6f2-112">Indica che questo cmdlet Reimposta il tasto di scelta principale.</span><span class="sxs-lookup"><span data-stu-id="7b6f2-112">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="7b6f2-113">-Key2</span><span class="sxs-lookup"><span data-stu-id="7b6f2-113">-Key2</span></span>
<span data-ttu-id="7b6f2-114">Indica che questo cmdlet Reimposta il tasto di scelta secondario.</span><span class="sxs-lookup"><span data-stu-id="7b6f2-114">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="7b6f2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b6f2-115">-ResourceGroupName</span></span>
<span data-ttu-id="7b6f2-116">Specifica il nome del gruppo di risorse della raccolta.</span><span class="sxs-lookup"><span data-stu-id="7b6f2-116">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="7b6f2-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="7b6f2-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="7b6f2-118">Specifica il nome della raccolta dell'area di lavoro di Power BI in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b6f2-118">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7b6f2-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b6f2-119">-Confirm</span></span>
<span data-ttu-id="7b6f2-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b6f2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b6f2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b6f2-121">-WhatIf</span></span>
<span data-ttu-id="7b6f2-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b6f2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b6f2-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b6f2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b6f2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b6f2-124">-DefaultProfile</span></span>
<span data-ttu-id="7b6f2-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b6f2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b6f2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b6f2-126">CommonParameters</span></span>
<span data-ttu-id="7b6f2-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b6f2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b6f2-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b6f2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b6f2-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b6f2-129">INPUTS</span></span>

## <span data-ttu-id="7b6f2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b6f2-130">OUTPUTS</span></span>

### <span data-ttu-id="7b6f2-131">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="7b6f2-131">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="7b6f2-132">Note</span><span class="sxs-lookup"><span data-stu-id="7b6f2-132">NOTES</span></span>

## <span data-ttu-id="7b6f2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b6f2-133">RELATED LINKS</span></span>

[<span data-ttu-id="7b6f2-134">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="7b6f2-134">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)

