---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-azcloudserviceremotedesktopextensionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
ms.openlocfilehash: 5ae7383f71524c87518b9f48cbb314bf74de633e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998212"
---
# <span data-ttu-id="ca1d5-101">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="ca1d5-101">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>

## <span data-ttu-id="ca1d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca1d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca1d5-103">Creare un oggetto in memoria per l'estensione desktop remoto</span><span class="sxs-lookup"><span data-stu-id="ca1d5-103">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="ca1d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca1d5-104">SYNTAX</span></span>

```
New-AzCloudServiceRemoteDesktopExtensionObject [-Name] <String> [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-TypeHandlerVersion] <String>] [[-RolesAppliedTo] <String[]>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="ca1d5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ca1d5-105">DESCRIPTION</span></span>
<span data-ttu-id="ca1d5-106">Creare un oggetto in memoria per l'estensione desktop remoto</span><span class="sxs-lookup"><span data-stu-id="ca1d5-106">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="ca1d5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca1d5-107">EXAMPLES</span></span>

### <span data-ttu-id="ca1d5-108">Esempio 1: Creare un oggetto estensione desktop remoto</span><span class="sxs-lookup"><span data-stu-id="ca1d5-108">Example 1: Create remote desktop extension object</span></span>
```powershell
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
```

<span data-ttu-id="ca1d5-109">Questo comando crea un oggetto estensione desktop remoto usato per creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ca1d5-109">This command creates remote desktop extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="ca1d5-110">Per altre informazioni, vedere New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="ca1d5-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="ca1d5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca1d5-111">PARAMETERS</span></span>

### <span data-ttu-id="ca1d5-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ca1d5-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ca1d5-113">Aggiornamento automatico della versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="ca1d5-113">Auto upgrade minor version.</span></span>

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

### <span data-ttu-id="ca1d5-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="ca1d5-114">-Credential</span></span>
<span data-ttu-id="ca1d5-115">Credenziali per l'estensione di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ca1d5-115">Credential for Remote Desktop Extension.</span></span>

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

### <span data-ttu-id="ca1d5-116">-Expiration</span><span class="sxs-lookup"><span data-stu-id="ca1d5-116">-Expiration</span></span>
<span data-ttu-id="ca1d5-117">Scadenza per l'estensione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ca1d5-117">Expiration for Remote Desktop Extension.</span></span>

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

### <span data-ttu-id="ca1d5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ca1d5-118">-Name</span></span>
<span data-ttu-id="ca1d5-119">Nome dell'estensione di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ca1d5-119">Name of Remote Desktop Extension.</span></span>

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

### <span data-ttu-id="ca1d5-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="ca1d5-120">-RolesAppliedTo</span></span>
<span data-ttu-id="ca1d5-121">Ruoli applicati a.</span><span class="sxs-lookup"><span data-stu-id="ca1d5-121">Roles applied to.</span></span>

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

### <span data-ttu-id="ca1d5-122">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ca1d5-122">-TypeHandlerVersion</span></span>
<span data-ttu-id="ca1d5-123">Versione dell'estensione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ca1d5-123">Remote Desktop Extension version.</span></span>

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

### <span data-ttu-id="ca1d5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca1d5-124">CommonParameters</span></span>
<span data-ttu-id="ca1d5-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca1d5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca1d5-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ca1d5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca1d5-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="ca1d5-127">INPUTS</span></span>

## <span data-ttu-id="ca1d5-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca1d5-128">OUTPUTS</span></span>

### <span data-ttu-id="ca1d5-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="ca1d5-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="ca1d5-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="ca1d5-130">NOTES</span></span>

<span data-ttu-id="ca1d5-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ca1d5-131">ALIASES</span></span>

## <span data-ttu-id="ca1d5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca1d5-132">RELATED LINKS</span></span>

