---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199854"
---
# <span data-ttu-id="282b0-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="282b0-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="282b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="282b0-102">SYNOPSIS</span></span>
<span data-ttu-id="282b0-103">Scarica e installa kubectl, lo strumento da riga di comando Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="282b0-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="282b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="282b0-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="282b0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="282b0-105">DESCRIPTION</span></span>
<span data-ttu-id="282b0-106">Scarica e installa kubectl, lo strumento da riga di comando Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="282b0-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="282b0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="282b0-107">EXAMPLES</span></span>

### <span data-ttu-id="282b0-108">Scarica e installa l'ultima versione di kubectl</span><span class="sxs-lookup"><span data-stu-id="282b0-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="282b0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="282b0-109">PARAMETERS</span></span>

### <span data-ttu-id="282b0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="282b0-110">-AsJob</span></span>
<span data-ttu-id="282b0-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="282b0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="282b0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="282b0-112">-DefaultProfile</span></span>
<span data-ttu-id="282b0-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="282b0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="282b0-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="282b0-114">-Destination</span></span>
<span data-ttu-id="282b0-115">Percorso in cui installare kubectl.</span><span class="sxs-lookup"><span data-stu-id="282b0-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="282b0-116">Per impostazione predefinita, installa in ~/.azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="282b0-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="282b0-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="282b0-117">-DownloadFromMirror</span></span>
<span data-ttu-id="282b0-118">Scarica dal sito mirror: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="282b0-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="282b0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="282b0-119">-Force</span></span>
<span data-ttu-id="282b0-120">Sovrascrivere il kubectl esistente senza chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="282b0-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="282b0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="282b0-121">-PassThru</span></span>
<span data-ttu-id="282b0-122">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="282b0-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="282b0-123">-Version</span><span class="sxs-lookup"><span data-stu-id="282b0-123">-Version</span></span>
<span data-ttu-id="282b0-124">Versione di kubectl da installare, ad esempio "v1.17.2".</span><span class="sxs-lookup"><span data-stu-id="282b0-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="282b0-125">Valore predefinito: Più recente</span><span class="sxs-lookup"><span data-stu-id="282b0-125">Default value: Latest</span></span>

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

### <span data-ttu-id="282b0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="282b0-126">-Confirm</span></span>
<span data-ttu-id="282b0-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="282b0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="282b0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="282b0-128">-WhatIf</span></span>
<span data-ttu-id="282b0-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="282b0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="282b0-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="282b0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="282b0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="282b0-131">CommonParameters</span></span>
<span data-ttu-id="282b0-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="282b0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="282b0-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="282b0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="282b0-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="282b0-134">INPUTS</span></span>

### <span data-ttu-id="282b0-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="282b0-135">None</span></span>

## <span data-ttu-id="282b0-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="282b0-136">OUTPUTS</span></span>

### <span data-ttu-id="282b0-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="282b0-137">System.Boolean</span></span>

## <span data-ttu-id="282b0-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="282b0-138">NOTES</span></span>

## <span data-ttu-id="282b0-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="282b0-139">RELATED LINKS</span></span>
