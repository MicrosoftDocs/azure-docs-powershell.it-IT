---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207427"
---
# <span data-ttu-id="83268-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="83268-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="83268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83268-102">SYNOPSIS</span></span>
<span data-ttu-id="83268-103">Aggiorna l'ereditarietà della configurazione di ritienizione dell'accesso al sito principale al sito SCM per un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="83268-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="83268-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83268-104">SYNTAX</span></span>

### <span data-ttu-id="83268-105">InputValuesParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83268-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83268-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83268-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83268-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="83268-107">DESCRIPTION</span></span>
<span data-ttu-id="83268-108">Il cmdlet **Update-AzWebAppAccessRestrictionConfig** aggiorna la configurazione di Restrizione di accesso per un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="83268-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="83268-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83268-109">EXAMPLES</span></span>

### <span data-ttu-id="83268-110">Esempio 1: Aggiornare un sito SCM di un'app Web per l'uso delle restrizioni di accesso dal sito principale</span><span class="sxs-lookup"><span data-stu-id="83268-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="83268-111">L'esempio seguente aggiorna un'app Web denominata IpRule che appartiene al gruppo di risorse MyResourceGroup per usare la configurazione delle restrizioni di accesso del sito principale nel sito scm.</span><span class="sxs-lookup"><span data-stu-id="83268-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="83268-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83268-112">PARAMETERS</span></span>

### <span data-ttu-id="83268-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83268-113">-DefaultProfile</span></span>
<span data-ttu-id="83268-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83268-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83268-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83268-115">-InputObject</span></span>
<span data-ttu-id="83268-116">Oggetto configurazione restrizione di accesso</span><span class="sxs-lookup"><span data-stu-id="83268-116">The access restriction config object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83268-117">-Name</span><span class="sxs-lookup"><span data-stu-id="83268-117">-Name</span></span>
<span data-ttu-id="83268-118">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="83268-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83268-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83268-119">-PassThru</span></span>
<span data-ttu-id="83268-120">Restituire l'oggetto configurazione della restrizione di accesso.</span><span class="sxs-lookup"><span data-stu-id="83268-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="83268-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83268-121">-ResourceGroupName</span></span>
<span data-ttu-id="83268-122">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="83268-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83268-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="83268-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="83268-124">Il sito Scm eredita le regole impostate nel sito principale.</span><span class="sxs-lookup"><span data-stu-id="83268-124">Scm site inherits rules set on Main site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83268-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="83268-125">-SlotName</span></span>
<span data-ttu-id="83268-126">Nome slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="83268-126">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83268-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83268-127">-Confirm</span></span>
<span data-ttu-id="83268-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83268-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83268-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83268-129">-WhatIf</span></span>
<span data-ttu-id="83268-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83268-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83268-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83268-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83268-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83268-132">CommonParameters</span></span>
<span data-ttu-id="83268-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83268-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83268-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="83268-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83268-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="83268-135">INPUTS</span></span>

### <span data-ttu-id="83268-136">System.String</span><span class="sxs-lookup"><span data-stu-id="83268-136">System.String</span></span>

### <span data-ttu-id="83268-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="83268-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="83268-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83268-138">OUTPUTS</span></span>

### <span data-ttu-id="83268-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="83268-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="83268-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="83268-140">NOTES</span></span>

## <span data-ttu-id="83268-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83268-141">RELATED LINKS</span></span>

[<span data-ttu-id="83268-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="83268-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="83268-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="83268-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="83268-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="83268-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
