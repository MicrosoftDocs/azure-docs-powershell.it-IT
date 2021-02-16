---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-azcloudserviceremotedesktopextensionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
ms.openlocfilehash: 022093b8fe1df28a151405a18009b40dd24b0c97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199422"
---
# <span data-ttu-id="469c2-101">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="469c2-101">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>

## <span data-ttu-id="469c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="469c2-102">SYNOPSIS</span></span>
<span data-ttu-id="469c2-103">Creare un oggetto in memoria per l'estensione desktop remoto</span><span class="sxs-lookup"><span data-stu-id="469c2-103">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="469c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="469c2-104">SYNTAX</span></span>

```
New-AzCloudServiceRemoteDesktopExtensionObject [-Name] <String> [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-TypeHandlerVersion] <String>] [[-RolesAppliedTo] <String[]>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="469c2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="469c2-105">DESCRIPTION</span></span>
<span data-ttu-id="469c2-106">Creare un oggetto in memoria per l'estensione desktop remoto</span><span class="sxs-lookup"><span data-stu-id="469c2-106">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="469c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="469c2-107">EXAMPLES</span></span>

### <span data-ttu-id="469c2-108">Esempio 1: Creare un oggetto estensione desktop remoto</span><span class="sxs-lookup"><span data-stu-id="469c2-108">Example 1: Create remote desktop extension object</span></span>
```powershell
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
```

<span data-ttu-id="469c2-109">Questo comando crea un oggetto estensione desktop remoto usato per creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="469c2-109">This command creates remote desktop extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="469c2-110">Per altre informazioni, vedere New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="469c2-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="469c2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="469c2-111">PARAMETERS</span></span>

### <span data-ttu-id="469c2-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="469c2-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="469c2-113">Aggiornamento automatico della versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="469c2-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="469c2-114">-Credential</span></span>
<span data-ttu-id="469c2-115">Credenziali per l'estensione di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="469c2-115">Credential for Remote Desktop Extension.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-116">-Expiration</span><span class="sxs-lookup"><span data-stu-id="469c2-116">-Expiration</span></span>
<span data-ttu-id="469c2-117">Scadenza per l'estensione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="469c2-117">Expiration for Remote Desktop Extension.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="469c2-118">-Name</span></span>
<span data-ttu-id="469c2-119">Nome dell'estensione di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="469c2-119">Name of Remote Desktop Extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="469c2-120">-RolesAppliedTo</span></span>
<span data-ttu-id="469c2-121">Ruoli applicati a.</span><span class="sxs-lookup"><span data-stu-id="469c2-121">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-122">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="469c2-122">-TypeHandlerVersion</span></span>
<span data-ttu-id="469c2-123">Versione dell'estensione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="469c2-123">Remote Desktop Extension version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469c2-124">CommonParameters</span></span>
<span data-ttu-id="469c2-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="469c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469c2-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="469c2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469c2-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="469c2-127">INPUTS</span></span>

## <span data-ttu-id="469c2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="469c2-128">OUTPUTS</span></span>

### <span data-ttu-id="469c2-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="469c2-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="469c2-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="469c2-130">NOTES</span></span>

<span data-ttu-id="469c2-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="469c2-131">ALIASES</span></span>

## <span data-ttu-id="469c2-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="469c2-132">RELATED LINKS</span></span>

