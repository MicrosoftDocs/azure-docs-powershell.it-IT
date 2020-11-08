---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94030899"
---
# <span data-ttu-id="2cf84-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="2cf84-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="2cf84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2cf84-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf84-103">Aggiorna l'ereditarietà della configurazione di Access restiction del sito principale in un sito SCM per una Web App Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf84-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="2cf84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cf84-104">SYNTAX</span></span>

### <span data-ttu-id="2cf84-105">InputValuesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2cf84-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cf84-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cf84-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cf84-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cf84-107">DESCRIPTION</span></span>
<span data-ttu-id="2cf84-108">Il cmdlet **Update-AzWebAppAccessRestrictionConfig** aggiorna la configurazione delle restrizioni di Access per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="2cf84-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="2cf84-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cf84-109">EXAMPLES</span></span>

### <span data-ttu-id="2cf84-110">Esempio 1: aggiornare un sito SCM di Web App per usare le restrizioni di accesso dal sito principale</span><span class="sxs-lookup"><span data-stu-id="2cf84-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="2cf84-111">L'esempio seguente aggiorna un'app Web denominata IpRule che appartiene al gruppo di risorse MyResourceGroup per usare la configurazione delle restrizioni di Access del sito principale nel sito SCM.</span><span class="sxs-lookup"><span data-stu-id="2cf84-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="2cf84-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2cf84-112">PARAMETERS</span></span>

### <span data-ttu-id="2cf84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf84-113">-DefaultProfile</span></span>
<span data-ttu-id="2cf84-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf84-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cf84-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cf84-115">-InputObject</span></span>
<span data-ttu-id="2cf84-116">Oggetto di configurazione restrizione di Access</span><span class="sxs-lookup"><span data-stu-id="2cf84-116">The access restriction config object</span></span>

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

### <span data-ttu-id="2cf84-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cf84-117">-Name</span></span>
<span data-ttu-id="2cf84-118">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="2cf84-118">WebApp Name</span></span>

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

### <span data-ttu-id="2cf84-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cf84-119">-PassThru</span></span>
<span data-ttu-id="2cf84-120">Restituisce l'oggetto di configurazione di restrizione di Access.</span><span class="sxs-lookup"><span data-stu-id="2cf84-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="2cf84-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf84-121">-ResourceGroupName</span></span>
<span data-ttu-id="2cf84-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="2cf84-122">Resource Group Name</span></span>

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

### <span data-ttu-id="2cf84-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="2cf84-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="2cf84-124">Il sito SCM eredita le regole impostate nel sito principale.</span><span class="sxs-lookup"><span data-stu-id="2cf84-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="2cf84-125">-Slotname</span><span class="sxs-lookup"><span data-stu-id="2cf84-125">-SlotName</span></span>
<span data-ttu-id="2cf84-126">Nome dello slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2cf84-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="2cf84-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2cf84-127">-Confirm</span></span>
<span data-ttu-id="2cf84-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cf84-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cf84-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cf84-129">-WhatIf</span></span>
<span data-ttu-id="2cf84-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2cf84-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2cf84-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2cf84-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cf84-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf84-132">CommonParameters</span></span>
<span data-ttu-id="2cf84-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf84-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf84-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cf84-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf84-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2cf84-135">INPUTS</span></span>

### <span data-ttu-id="2cf84-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2cf84-136">System.String</span></span>

### <span data-ttu-id="2cf84-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2cf84-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2cf84-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cf84-138">OUTPUTS</span></span>

### <span data-ttu-id="2cf84-139">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="2cf84-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="2cf84-140">Note</span><span class="sxs-lookup"><span data-stu-id="2cf84-140">NOTES</span></span>

## <span data-ttu-id="2cf84-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cf84-141">RELATED LINKS</span></span>

[<span data-ttu-id="2cf84-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="2cf84-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="2cf84-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="2cf84-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="2cf84-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="2cf84-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
