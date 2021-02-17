---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191398"
---
# <span data-ttu-id="dfcf9-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="dfcf9-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="dfcf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfcf9-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcf9-103">Reimposta il tasto di scelta specificato.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-103">Resets the specified access key.</span></span>

## <span data-ttu-id="dfcf9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfcf9-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfcf9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dfcf9-105">DESCRIPTION</span></span>
<span data-ttu-id="dfcf9-106">Il cmdlet **Reset-AzPowerBIWorkspaceCollectionAccessKey** reimposta la chiave di accesso specificata nella raccolta dell'area di lavoro di Power BI.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="dfcf9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfcf9-107">EXAMPLES</span></span>

### <span data-ttu-id="dfcf9-108">Esempio 1: Reimpostare la chiave di accesso primaria</span><span class="sxs-lookup"><span data-stu-id="dfcf9-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="dfcf9-109">Questo comando reimposta la chiave di accesso primaria per la raccolta dell'area di lavoro denominata WCN11 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="dfcf9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfcf9-110">PARAMETERS</span></span>

### <span data-ttu-id="dfcf9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcf9-111">-DefaultProfile</span></span>
<span data-ttu-id="dfcf9-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="dfcf9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfcf9-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="dfcf9-113">-Key1</span></span>
<span data-ttu-id="dfcf9-114">Indica che questo cmdlet reimposta la chiave di accesso primaria.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="dfcf9-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="dfcf9-115">-Key2</span></span>
<span data-ttu-id="dfcf9-116">Indica che questo cmdlet reimposta la chiave di accesso secondaria.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="dfcf9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfcf9-117">-ResourceGroupName</span></span>
<span data-ttu-id="dfcf9-118">Specifica il nome del gruppo di risorse della raccolta.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="dfcf9-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="dfcf9-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="dfcf9-120">Specifica il nome della raccolta dell'area di lavoro di Power BI su cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="dfcf9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfcf9-121">-Confirm</span></span>
<span data-ttu-id="dfcf9-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfcf9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfcf9-123">-WhatIf</span></span>
<span data-ttu-id="dfcf9-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfcf9-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfcf9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcf9-126">CommonParameters</span></span>
<span data-ttu-id="dfcf9-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcf9-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfcf9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcf9-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="dfcf9-129">INPUTS</span></span>

### <span data-ttu-id="dfcf9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="dfcf9-130">System.String</span></span>

## <span data-ttu-id="dfcf9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfcf9-131">OUTPUTS</span></span>

### <span data-ttu-id="dfcf9-132">Microsoft.Azure.Commands.Management.PowerBIE systemdded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="dfcf9-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="dfcf9-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="dfcf9-133">NOTES</span></span>

## <span data-ttu-id="dfcf9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfcf9-134">RELATED LINKS</span></span>

[<span data-ttu-id="dfcf9-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="dfcf9-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


