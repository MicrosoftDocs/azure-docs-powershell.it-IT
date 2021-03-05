---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 6a3dc975c34d4938235ce95743f73f833a948b49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966846"
---
# <span data-ttu-id="7d427-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="7d427-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="7d427-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d427-102">SYNOPSIS</span></span>
<span data-ttu-id="7d427-103">Scarica e installa kubectl, lo strumento da riga di comando Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7d427-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="7d427-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d427-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d427-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d427-105">DESCRIPTION</span></span>
<span data-ttu-id="7d427-106">Scarica e installa kubectl, lo strumento da riga di comando Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7d427-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="7d427-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d427-107">EXAMPLES</span></span>

### <span data-ttu-id="7d427-108">Scarica e installa l'ultima versione di kubectl</span><span class="sxs-lookup"><span data-stu-id="7d427-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="7d427-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d427-109">PARAMETERS</span></span>

### <span data-ttu-id="7d427-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d427-110">-AsJob</span></span>
<span data-ttu-id="7d427-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7d427-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d427-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d427-112">-DefaultProfile</span></span>
<span data-ttu-id="7d427-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d427-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d427-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="7d427-114">-Destination</span></span>
<span data-ttu-id="7d427-115">Percorso in cui installare kubectl.</span><span class="sxs-lookup"><span data-stu-id="7d427-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="7d427-116">Per impostazione predefinita, installa in ~/.azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="7d427-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="7d427-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="7d427-117">-DownloadFromMirror</span></span>
<span data-ttu-id="7d427-118">Scarica dal sito mirror: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="7d427-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="7d427-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7d427-119">-Force</span></span>
<span data-ttu-id="7d427-120">Sovrascrivere il kubectl esistente senza chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="7d427-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="7d427-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d427-121">-PassThru</span></span>
<span data-ttu-id="7d427-122">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="7d427-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7d427-123">-Version</span><span class="sxs-lookup"><span data-stu-id="7d427-123">-Version</span></span>
<span data-ttu-id="7d427-124">Versione di kubectl da installare, ad esempio "v1.17.2".</span><span class="sxs-lookup"><span data-stu-id="7d427-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="7d427-125">Valore predefinito: Più recente</span><span class="sxs-lookup"><span data-stu-id="7d427-125">Default value: Latest</span></span>

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

### <span data-ttu-id="7d427-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d427-126">-Confirm</span></span>
<span data-ttu-id="7d427-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d427-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d427-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d427-128">-WhatIf</span></span>
<span data-ttu-id="7d427-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d427-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d427-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d427-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d427-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d427-131">CommonParameters</span></span>
<span data-ttu-id="7d427-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d427-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d427-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7d427-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d427-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d427-134">INPUTS</span></span>

### <span data-ttu-id="7d427-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7d427-135">None</span></span>

## <span data-ttu-id="7d427-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d427-136">OUTPUTS</span></span>

### <span data-ttu-id="7d427-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7d427-137">System.Boolean</span></span>

## <span data-ttu-id="7d427-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d427-138">NOTES</span></span>

## <span data-ttu-id="7d427-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d427-139">RELATED LINKS</span></span>
