---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceExtensionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
ms.openlocfilehash: d37a717ba87771310de4f1944e3865712e00554e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986186"
---
# <span data-ttu-id="2979a-101">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="2979a-101">New-AzCloudServiceExtensionObject</span></span>

## <span data-ttu-id="2979a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2979a-102">SYNOPSIS</span></span>
<span data-ttu-id="2979a-103">Creare un oggetto in memoria per l'estensione</span><span class="sxs-lookup"><span data-stu-id="2979a-103">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="2979a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2979a-104">SYNTAX</span></span>

```
New-AzCloudServiceExtensionObject [-AutoUpgradeMinorVersion <Boolean>] [-Name <String>]
 [-ProtectedSetting <String>] [-Publisher <String>] [-RolesAppliedTo <String[]>] [-Setting <String>]
 [-Type <String>] [-TypeHandlerVersion <String>] [<CommonParameters>]
```

## <span data-ttu-id="2979a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2979a-105">DESCRIPTION</span></span>
<span data-ttu-id="2979a-106">Creare un oggetto in memoria per l'estensione</span><span class="sxs-lookup"><span data-stu-id="2979a-106">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="2979a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2979a-107">EXAMPLES</span></span>

### <span data-ttu-id="2979a-108">Esempio 1: Creare un oggetto di estensione di questo tipo</span><span class="sxs-lookup"><span data-stu-id="2979a-108">Example 1: Create Geneva extension object</span></span>
```powershell
PS C:\> $extension = New-AzCloudServiceExtensionObject -Name "GenevaExtension" -Publisher "Microsoft.Azure.Geneva" -Type "GenevaMonitoringPaaS" -TypeHandlerVersion "2.14.0.2"
```

<span data-ttu-id="2979a-109">Questo comando crea un oggetto estensione di questo tipo, usato per creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="2979a-109">This command creates Geneva extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="2979a-110">Per altre informazioni, vedere New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="2979a-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="2979a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2979a-111">PARAMETERS</span></span>

### <span data-ttu-id="2979a-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2979a-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2979a-113">Specificare in modo esplicito se CRP può eseguire automaticamente l'aggiornamento di typeHandlerVersion alle versioni secondarie successive quando diventano disponibili.</span><span class="sxs-lookup"><span data-stu-id="2979a-113">Explicitly specify whether CRP can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2979a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="2979a-114">-Name</span></span>
<span data-ttu-id="2979a-115">Nome.</span><span class="sxs-lookup"><span data-stu-id="2979a-115">Name.</span></span>

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

### <span data-ttu-id="2979a-116">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="2979a-116">-ProtectedSetting</span></span>
<span data-ttu-id="2979a-117">Impostazioni protette per l'estensione, crittografate prima dell'invio alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2979a-117">Protected settings for the extension which are encrypted before sent to the VM.</span></span>

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

### <span data-ttu-id="2979a-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2979a-118">-Publisher</span></span>
<span data-ttu-id="2979a-119">Publisher.</span><span class="sxs-lookup"><span data-stu-id="2979a-119">Publisher.</span></span>

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

### <span data-ttu-id="2979a-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="2979a-120">-RolesAppliedTo</span></span>
<span data-ttu-id="2979a-121">RolesAppliedTo.</span><span class="sxs-lookup"><span data-stu-id="2979a-121">RolesAppliedTo.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2979a-122">-Setting</span><span class="sxs-lookup"><span data-stu-id="2979a-122">-Setting</span></span>
<span data-ttu-id="2979a-123">Impostazioni pubbliche per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="2979a-123">Public settings for the extension.</span></span>

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

### <span data-ttu-id="2979a-124">-Type</span><span class="sxs-lookup"><span data-stu-id="2979a-124">-Type</span></span>
<span data-ttu-id="2979a-125">Digitare.</span><span class="sxs-lookup"><span data-stu-id="2979a-125">Type.</span></span>

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

### <span data-ttu-id="2979a-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2979a-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="2979a-127">TypeHandlerVersion.</span><span class="sxs-lookup"><span data-stu-id="2979a-127">TypeHandlerVersion.</span></span>

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

### <span data-ttu-id="2979a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2979a-128">CommonParameters</span></span>
<span data-ttu-id="2979a-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2979a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2979a-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2979a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2979a-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="2979a-131">INPUTS</span></span>

## <span data-ttu-id="2979a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2979a-132">OUTPUTS</span></span>

### <span data-ttu-id="2979a-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="2979a-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="2979a-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="2979a-134">NOTES</span></span>

<span data-ttu-id="2979a-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2979a-135">ALIASES</span></span>

## <span data-ttu-id="2979a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2979a-136">RELATED LINKS</span></span>

