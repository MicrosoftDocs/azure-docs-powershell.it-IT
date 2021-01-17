---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479119"
---
# <span data-ttu-id="7154a-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="7154a-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="7154a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7154a-102">SYNOPSIS</span></span>
<span data-ttu-id="7154a-103">Scaricare e installare kubectl, lo strumento da riga di comando Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7154a-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="7154a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7154a-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7154a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7154a-105">DESCRIPTION</span></span>
<span data-ttu-id="7154a-106">Scaricare e installare kubectl, lo strumento da riga di comando Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7154a-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="7154a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7154a-107">EXAMPLES</span></span>

### <span data-ttu-id="7154a-108">Scaricare e installare la versione più recente di kubectl</span><span class="sxs-lookup"><span data-stu-id="7154a-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="7154a-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7154a-109">PARAMETERS</span></span>

### <span data-ttu-id="7154a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7154a-110">-AsJob</span></span>
<span data-ttu-id="7154a-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7154a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7154a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7154a-112">-DefaultProfile</span></span>
<span data-ttu-id="7154a-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7154a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7154a-114">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="7154a-114">-Destination</span></span>
<span data-ttu-id="7154a-115">Percorso in cui installare kubectl.</span><span class="sxs-lookup"><span data-stu-id="7154a-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="7154a-116">Impostazione predefinita per l'installazione in ~/.Azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="7154a-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="7154a-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="7154a-117">-DownloadFromMirror</span></span>
<span data-ttu-id="7154a-118">Scarica dal sito mirror: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="7154a-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="7154a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7154a-119">-Force</span></span>
<span data-ttu-id="7154a-120">Sovrascrivere kubectl esistenti senza richiesta</span><span class="sxs-lookup"><span data-stu-id="7154a-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="7154a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7154a-121">-PassThru</span></span>
<span data-ttu-id="7154a-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7154a-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7154a-123">-Versione</span><span class="sxs-lookup"><span data-stu-id="7154a-123">-Version</span></span>
<span data-ttu-id="7154a-124">Versione di kubectl da installare, ad esempio "v 1.17.2".</span><span class="sxs-lookup"><span data-stu-id="7154a-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="7154a-125">Valore predefinito: ultimo</span><span class="sxs-lookup"><span data-stu-id="7154a-125">Default value: Latest</span></span>

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

### <span data-ttu-id="7154a-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7154a-126">-Confirm</span></span>
<span data-ttu-id="7154a-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7154a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7154a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7154a-128">-WhatIf</span></span>
<span data-ttu-id="7154a-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7154a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7154a-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7154a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7154a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7154a-131">CommonParameters</span></span>
<span data-ttu-id="7154a-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7154a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7154a-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7154a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7154a-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7154a-134">INPUTS</span></span>

### <span data-ttu-id="7154a-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7154a-135">None</span></span>

## <span data-ttu-id="7154a-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7154a-136">OUTPUTS</span></span>

### <span data-ttu-id="7154a-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7154a-137">System.Boolean</span></span>

## <span data-ttu-id="7154a-138">Note</span><span class="sxs-lookup"><span data-stu-id="7154a-138">NOTES</span></span>

## <span data-ttu-id="7154a-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7154a-139">RELATED LINKS</span></span>
