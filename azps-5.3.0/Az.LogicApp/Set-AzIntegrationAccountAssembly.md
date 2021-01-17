---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474096"
---
# <span data-ttu-id="5dccf-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5dccf-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="5dccf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5dccf-102">SYNOPSIS</span></span>
<span data-ttu-id="5dccf-103">Modifica un assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5dccf-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="5dccf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5dccf-104">SYNTAX</span></span>

### <span data-ttu-id="5dccf-105">ByIntegrationAccountAndFilePath (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5dccf-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dccf-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="5dccf-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5dccf-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="5dccf-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5dccf-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="5dccf-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dccf-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="5dccf-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dccf-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="5dccf-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dccf-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="5dccf-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dccf-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="5dccf-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dccf-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="5dccf-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dccf-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dccf-114">DESCRIPTION</span></span>
<span data-ttu-id="5dccf-115">Il cmdlet **set-AzIntegrationAccountAssembly** modifica un assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5dccf-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="5dccf-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5dccf-116">EXAMPLES</span></span>

### <span data-ttu-id="5dccf-117">Esempio 1: modificare un assembly usando un file locale</span><span class="sxs-lookup"><span data-stu-id="5dccf-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="5dccf-118">Modifica l'assembly denominato "sampleAssembly" usando il file locale che si trova nel percorso del file contenuto in "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="5dccf-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="5dccf-119">Esempio 2: modificare un assembly usando i dati di byte</span><span class="sxs-lookup"><span data-stu-id="5dccf-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="5dccf-120">Modifica l'assembly denominato "sampleAssembly" usando la matrice di byte contenuta in "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="5dccf-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="5dccf-121">Esempio 3: modificare un assembly usando un collegamento contenuto</span><span class="sxs-lookup"><span data-stu-id="5dccf-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="5dccf-122">Modifica l'assembly denominato "sampleAssembly" usando i dati a byte presenti nell'URL "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="5dccf-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="5dccf-123">Questo è il metodo suggerito per la creazione di assembly di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="5dccf-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="5dccf-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5dccf-124">PARAMETERS</span></span>

### <span data-ttu-id="5dccf-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="5dccf-125">-AssemblyData</span></span>
<span data-ttu-id="5dccf-126">Dati del byte dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5dccf-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dccf-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="5dccf-127">-AssemblyFilePath</span></span>
<span data-ttu-id="5dccf-128">Percorso del file dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5dccf-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dccf-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="5dccf-129">-ContentLink</span></span>
<span data-ttu-id="5dccf-130">Un collegamento accessibile pubblicamente ai dati dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5dccf-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dccf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dccf-131">-DefaultProfile</span></span>
<span data-ttu-id="5dccf-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5dccf-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dccf-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5dccf-133">-InputObject</span></span>
<span data-ttu-id="5dccf-134">Un assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5dccf-134">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dccf-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5dccf-135">-Metadata</span></span>
<span data-ttu-id="5dccf-136">Metadati dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5dccf-136">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dccf-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="5dccf-137">-Name</span></span>
<span data-ttu-id="5dccf-138">Nome dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5dccf-138">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dccf-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="5dccf-139">-ParentName</span></span>
<span data-ttu-id="5dccf-140">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5dccf-140">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dccf-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dccf-141">-ResourceGroupName</span></span>
<span data-ttu-id="5dccf-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5dccf-142">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dccf-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5dccf-143">-ResourceId</span></span>
<span data-ttu-id="5dccf-144">ID risorsa dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5dccf-144">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dccf-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5dccf-145">-Confirm</span></span>
<span data-ttu-id="5dccf-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dccf-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dccf-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dccf-147">-WhatIf</span></span>
<span data-ttu-id="5dccf-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5dccf-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5dccf-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5dccf-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dccf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dccf-150">CommonParameters</span></span>
<span data-ttu-id="5dccf-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dccf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dccf-152">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dccf-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dccf-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5dccf-153">INPUTS</span></span>

### <span data-ttu-id="5dccf-154">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5dccf-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="5dccf-155">System. String</span><span class="sxs-lookup"><span data-stu-id="5dccf-155">System.String</span></span>

## <span data-ttu-id="5dccf-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5dccf-156">OUTPUTS</span></span>

### <span data-ttu-id="5dccf-157">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5dccf-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="5dccf-158">Note</span><span class="sxs-lookup"><span data-stu-id="5dccf-158">NOTES</span></span>

## <span data-ttu-id="5dccf-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5dccf-159">RELATED LINKS</span></span>
