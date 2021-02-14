---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceExtensionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
ms.openlocfilehash: 761d34b4ed2d061b773c136a7d4e2db9f05a9103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195135"
---
# <span data-ttu-id="b96de-101">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="b96de-101">New-AzCloudServiceExtensionObject</span></span>

## <span data-ttu-id="b96de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b96de-102">SYNOPSIS</span></span>
<span data-ttu-id="b96de-103">Creare un oggetto in memoria per l'estensione</span><span class="sxs-lookup"><span data-stu-id="b96de-103">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="b96de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b96de-104">SYNTAX</span></span>

```
New-AzCloudServiceExtensionObject [-AutoUpgradeMinorVersion <Boolean>] [-Name <String>]
 [-ProtectedSetting <String>] [-Publisher <String>] [-RolesAppliedTo <String[]>] [-Setting <String>]
 [-Type <String>] [-TypeHandlerVersion <String>] [<CommonParameters>]
```

## <span data-ttu-id="b96de-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b96de-105">DESCRIPTION</span></span>
<span data-ttu-id="b96de-106">Creare un oggetto in memoria per l'estensione</span><span class="sxs-lookup"><span data-stu-id="b96de-106">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="b96de-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b96de-107">EXAMPLES</span></span>

### <span data-ttu-id="b96de-108">Esempio 1: Creare un oggetto di estensione di questo tipo</span><span class="sxs-lookup"><span data-stu-id="b96de-108">Example 1: Create Geneva extension object</span></span>
```powershell
PS C:\> $extension = New-AzCloudServiceExtensionObject -Name "GenevaExtension" -Publisher "Microsoft.Azure.Geneva" -Type "GenevaMonitoringPaaS" -TypeHandlerVersion "2.14.0.2"
```

<span data-ttu-id="b96de-109">Questo comando crea un oggetto estensione di questo tipo, usato per creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b96de-109">This command creates Geneva extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="b96de-110">Per altre informazioni, vedere New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="b96de-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="b96de-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b96de-111">PARAMETERS</span></span>

### <span data-ttu-id="b96de-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b96de-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b96de-113">Specificare in modo esplicito se CRP può eseguire automaticamente l'aggiornamento di typeHandlerVersion alle versioni secondarie successive quando diventano disponibili.</span><span class="sxs-lookup"><span data-stu-id="b96de-113">Explicitly specify whether CRP can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>

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

### <span data-ttu-id="b96de-114">-Name</span><span class="sxs-lookup"><span data-stu-id="b96de-114">-Name</span></span>
<span data-ttu-id="b96de-115">Nome.</span><span class="sxs-lookup"><span data-stu-id="b96de-115">Name.</span></span>

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

### <span data-ttu-id="b96de-116">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="b96de-116">-ProtectedSetting</span></span>
<span data-ttu-id="b96de-117">Impostazioni protette per l'estensione, crittografate prima dell'invio alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b96de-117">Protected settings for the extension which are encrypted before sent to the VM.</span></span>

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

### <span data-ttu-id="b96de-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b96de-118">-Publisher</span></span>
<span data-ttu-id="b96de-119">Publisher.</span><span class="sxs-lookup"><span data-stu-id="b96de-119">Publisher.</span></span>

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

### <span data-ttu-id="b96de-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="b96de-120">-RolesAppliedTo</span></span>
<span data-ttu-id="b96de-121">RolesAppliedTo.</span><span class="sxs-lookup"><span data-stu-id="b96de-121">RolesAppliedTo.</span></span>

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

### <span data-ttu-id="b96de-122">-Setting</span><span class="sxs-lookup"><span data-stu-id="b96de-122">-Setting</span></span>
<span data-ttu-id="b96de-123">Impostazioni pubbliche per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="b96de-123">Public settings for the extension.</span></span>

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

### <span data-ttu-id="b96de-124">-Type</span><span class="sxs-lookup"><span data-stu-id="b96de-124">-Type</span></span>
<span data-ttu-id="b96de-125">Digitare.</span><span class="sxs-lookup"><span data-stu-id="b96de-125">Type.</span></span>

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

### <span data-ttu-id="b96de-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b96de-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="b96de-127">TypeHandlerVersion.</span><span class="sxs-lookup"><span data-stu-id="b96de-127">TypeHandlerVersion.</span></span>

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

### <span data-ttu-id="b96de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b96de-128">CommonParameters</span></span>
<span data-ttu-id="b96de-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b96de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b96de-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b96de-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b96de-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="b96de-131">INPUTS</span></span>

## <span data-ttu-id="b96de-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b96de-132">OUTPUTS</span></span>

### <span data-ttu-id="b96de-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="b96de-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="b96de-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="b96de-134">NOTES</span></span>

<span data-ttu-id="b96de-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b96de-135">ALIASES</span></span>

## <span data-ttu-id="b96de-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b96de-136">RELATED LINKS</span></span>

