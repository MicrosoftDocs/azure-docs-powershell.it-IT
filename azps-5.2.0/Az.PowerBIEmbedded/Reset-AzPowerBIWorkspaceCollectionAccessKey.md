---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345475"
---
# <span data-ttu-id="9f38d-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="9f38d-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="9f38d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f38d-102">SYNOPSIS</span></span>
<span data-ttu-id="9f38d-103">Reimposta il tasto di scelta specificato.</span><span class="sxs-lookup"><span data-stu-id="9f38d-103">Resets the specified access key.</span></span>

## <span data-ttu-id="9f38d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f38d-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f38d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f38d-105">DESCRIPTION</span></span>
<span data-ttu-id="9f38d-106">Il cmdlet **Reset-AzPowerBIWorkspaceCollectionAccessKey** Reimposta il codice di accesso specificato nella raccolta dell'area di lavoro di Power bi.</span><span class="sxs-lookup"><span data-stu-id="9f38d-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="9f38d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f38d-107">EXAMPLES</span></span>

### <span data-ttu-id="9f38d-108">Esempio 1: reimpostare il tasto di scelta principale</span><span class="sxs-lookup"><span data-stu-id="9f38d-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="9f38d-109">Questo comando Reimposta il codice di accesso principale per la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="9f38d-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="9f38d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f38d-110">PARAMETERS</span></span>

### <span data-ttu-id="9f38d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f38d-111">-DefaultProfile</span></span>
<span data-ttu-id="9f38d-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9f38d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f38d-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="9f38d-113">-Key1</span></span>
<span data-ttu-id="9f38d-114">Indica che questo cmdlet Reimposta il tasto di scelta principale.</span><span class="sxs-lookup"><span data-stu-id="9f38d-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="9f38d-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="9f38d-115">-Key2</span></span>
<span data-ttu-id="9f38d-116">Indica che questo cmdlet Reimposta il tasto di scelta secondario.</span><span class="sxs-lookup"><span data-stu-id="9f38d-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="9f38d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f38d-117">-ResourceGroupName</span></span>
<span data-ttu-id="9f38d-118">Specifica il nome del gruppo di risorse della raccolta.</span><span class="sxs-lookup"><span data-stu-id="9f38d-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="9f38d-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="9f38d-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="9f38d-120">Specifica il nome della raccolta dell'area di lavoro di Power BI in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f38d-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9f38d-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9f38d-121">-Confirm</span></span>
<span data-ttu-id="9f38d-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f38d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f38d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f38d-123">-WhatIf</span></span>
<span data-ttu-id="9f38d-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f38d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f38d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f38d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f38d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f38d-126">CommonParameters</span></span>
<span data-ttu-id="9f38d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f38d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f38d-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f38d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f38d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f38d-129">INPUTS</span></span>

### <span data-ttu-id="9f38d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9f38d-130">System.String</span></span>

## <span data-ttu-id="9f38d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f38d-131">OUTPUTS</span></span>

### <span data-ttu-id="9f38d-132">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="9f38d-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="9f38d-133">Note</span><span class="sxs-lookup"><span data-stu-id="9f38d-133">NOTES</span></span>

## <span data-ttu-id="9f38d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f38d-134">RELATED LINKS</span></span>

[<span data-ttu-id="9f38d-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="9f38d-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


