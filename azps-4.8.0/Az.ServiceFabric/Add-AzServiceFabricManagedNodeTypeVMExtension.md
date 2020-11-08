---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191918"
---
# <span data-ttu-id="03b39-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="03b39-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="03b39-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03b39-102">SYNOPSIS</span></span>
<span data-ttu-id="03b39-103">Aggiungere l'estensione VM al tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="03b39-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="03b39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03b39-104">SYNTAX</span></span>

### <span data-ttu-id="03b39-105">ByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03b39-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03b39-106">ByName</span><span class="sxs-lookup"><span data-stu-id="03b39-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03b39-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03b39-107">DESCRIPTION</span></span>
<span data-ttu-id="03b39-108">Aggiungere l'estensione VM al tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="03b39-108">Add vm extension to the node type.</span></span> <span data-ttu-id="03b39-109">In questo modo si aggiungerà l'estensione alla risorsa set di scala della macchina virtuale underliying.</span><span class="sxs-lookup"><span data-stu-id="03b39-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="03b39-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03b39-110">EXAMPLES</span></span>

### <span data-ttu-id="03b39-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="03b39-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="03b39-112">Questo comando aggiunge un'estensione al tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="03b39-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="03b39-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="03b39-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="03b39-114">Questo comando aggiunge un'estensione con le impostazioni e le impostazioni protette al tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="03b39-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="03b39-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="03b39-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="03b39-116">Questo comando aggiunge un'estensione al tipo di nodo, con piping.</span><span class="sxs-lookup"><span data-stu-id="03b39-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="03b39-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03b39-117">PARAMETERS</span></span>

### <span data-ttu-id="03b39-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03b39-118">-AsJob</span></span>
<span data-ttu-id="03b39-119">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="03b39-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="03b39-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="03b39-121">Indica se l'estensione deve usare una versione secondaria più recente, se disponibile in fase di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="03b39-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="03b39-122">Una volta distribuita, tuttavia, l'estensione non aggiornerà le versioni secondarie, a meno che non vengano ridistribuite, anche se questa proprietà è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="03b39-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-123">-Clustername</span><span class="sxs-lookup"><span data-stu-id="03b39-123">-ClusterName</span></span>
<span data-ttu-id="03b39-124">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="03b39-124">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b39-125">-DefaultProfile</span></span>
<span data-ttu-id="03b39-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03b39-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="03b39-127">-ForceUpdateTag</span></span>
<span data-ttu-id="03b39-128">Se viene specificato un valore ed è diverso dal valore precedente, il gestore dell'estensione verrà costretto all'aggiornamento anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="03b39-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03b39-129">-InputObject</span></span>
<span data-ttu-id="03b39-130">Risorsa tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="03b39-130">Node Type resource</span></span>

```yaml
Type: PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="03b39-131">-Name</span></span>
<span data-ttu-id="03b39-132">nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="03b39-132">extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="03b39-133">-NodeTypeName</span></span>
<span data-ttu-id="03b39-134">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="03b39-134">Specify the name of the node type.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="03b39-135">-ProtectedSetting</span></span>
<span data-ttu-id="03b39-136">L'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="03b39-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="03b39-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="03b39-138">Raccolta di nomi di estensione dopo cui deve essere effettuato il provisioning di questa estensione.</span><span class="sxs-lookup"><span data-stu-id="03b39-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="03b39-139">-Publisher</span></span>
<span data-ttu-id="03b39-140">Nome dell'autore del gestore di estensione.</span><span class="sxs-lookup"><span data-stu-id="03b39-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="03b39-141">Questo può usare il cmdlet Get-AzVMImagePublisher per ottenere il Publisher.</span><span class="sxs-lookup"><span data-stu-id="03b39-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b39-142">-ResourceGroupName</span></span>
<span data-ttu-id="03b39-143">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="03b39-143">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-144">-Impostazione</span><span class="sxs-lookup"><span data-stu-id="03b39-144">-Setting</span></span>
<span data-ttu-id="03b39-145">Impostazioni pubbliche in formato JSON per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="03b39-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-146">-Digitare</span><span class="sxs-lookup"><span data-stu-id="03b39-146">-Type</span></span>
<span data-ttu-id="03b39-147">Specifica il tipo di estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="03b39-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="03b39-148">Puoi usare il cmdlet Get-AzVMExtensionImageType per ottenere il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="03b39-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="03b39-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="03b39-150">Specifica la versione del gestore di script.</span><span class="sxs-lookup"><span data-stu-id="03b39-150">Specifies the version of the script handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="03b39-151">-Confirm</span></span>
<span data-ttu-id="03b39-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03b39-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03b39-153">-WhatIf</span></span>
<span data-ttu-id="03b39-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03b39-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03b39-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03b39-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b39-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b39-156">CommonParameters</span></span>
<span data-ttu-id="03b39-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b39-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b39-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03b39-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b39-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03b39-159">INPUTS</span></span>

### <span data-ttu-id="03b39-160">System. String</span><span class="sxs-lookup"><span data-stu-id="03b39-160">System.String</span></span>

### <span data-ttu-id="03b39-161">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="03b39-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="03b39-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03b39-162">OUTPUTS</span></span>

### <span data-ttu-id="03b39-163">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="03b39-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="03b39-164">Note</span><span class="sxs-lookup"><span data-stu-id="03b39-164">NOTES</span></span>

## <span data-ttu-id="03b39-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03b39-165">RELATED LINKS</span></span>
