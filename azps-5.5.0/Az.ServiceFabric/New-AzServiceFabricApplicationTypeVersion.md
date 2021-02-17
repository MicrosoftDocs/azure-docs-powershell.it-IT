---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 60065541ecdd8439b67f4370bc1ef8bdc24119bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198654"
---
# <span data-ttu-id="a84c0-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a84c0-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="a84c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a84c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a84c0-103">Creare una nuova versione del tipo di applicazione nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="a84c0-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="a84c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a84c0-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a84c0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a84c0-105">DESCRIPTION</span></span>
<span data-ttu-id="a84c0-106">Questo cmdlet crea una nuova versione del tipo di applicazione usando il pacchetto specificato in -PackageUrl. Questo deve essere accessibile tramite un endpoint REST in modo che Gestione risorse di Azure utilizzi durante la distribuzione e contenesse l'applicazione compressa con estensione sfpkg.</span><span class="sxs-lookup"><span data-stu-id="a84c0-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="a84c0-107">Questo comando crea il tipo di applicazione, se non esiste già.</span><span class="sxs-lookup"><span data-stu-id="a84c0-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="a84c0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a84c0-108">EXAMPLES</span></span>

### <span data-ttu-id="a84c0-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a84c0-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="a84c0-110">Questo esempio crea una versione del tipo di applicazione "v1" nel tipo "testAppType".</span><span class="sxs-lookup"><span data-stu-id="a84c0-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="a84c0-111">La versione nel manifesto dell'applicazione contenuta nel pacchetto deve avere la stessa versione di quella specificata in -Version.</span><span class="sxs-lookup"><span data-stu-id="a84c0-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="a84c0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a84c0-112">PARAMETERS</span></span>

### <span data-ttu-id="a84c0-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a84c0-113">-ClusterName</span></span>
<span data-ttu-id="a84c0-114">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="a84c0-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a84c0-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="a84c0-115">-DefaultParameter</span></span>
<span data-ttu-id="a84c0-116">Specificare i valori predefiniti dei parametri dell'applicazione come coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="a84c0-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="a84c0-117">Questi parametri devono essere presenti nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a84c0-117">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a84c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a84c0-118">-DefaultProfile</span></span>
<span data-ttu-id="a84c0-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a84c0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a84c0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a84c0-120">-Force</span></span>
<span data-ttu-id="a84c0-121">Continuare senza chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="a84c0-121">Continue without prompts</span></span>

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

### <span data-ttu-id="a84c0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a84c0-122">-Name</span></span>
<span data-ttu-id="a84c0-123">Specificare il nome del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="a84c0-123">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84c0-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="a84c0-124">-PackageUrl</span></span>
<span data-ttu-id="a84c0-125">Specificare l'URL del file sfpkg del pacchetto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="a84c0-125">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a84c0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a84c0-126">-ResourceGroupName</span></span>
<span data-ttu-id="a84c0-127">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a84c0-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a84c0-128">-Version</span><span class="sxs-lookup"><span data-stu-id="a84c0-128">-Version</span></span>
<span data-ttu-id="a84c0-129">Specificare la versione del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="a84c0-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84c0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a84c0-130">-Confirm</span></span>
<span data-ttu-id="a84c0-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a84c0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a84c0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a84c0-132">-WhatIf</span></span>
<span data-ttu-id="a84c0-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a84c0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a84c0-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a84c0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a84c0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a84c0-135">CommonParameters</span></span>
<span data-ttu-id="a84c0-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a84c0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a84c0-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a84c0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a84c0-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="a84c0-138">INPUTS</span></span>

### <span data-ttu-id="a84c0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a84c0-139">System.String</span></span>

### <span data-ttu-id="a84c0-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a84c0-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a84c0-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a84c0-141">OUTPUTS</span></span>

### <span data-ttu-id="a84c0-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a84c0-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="a84c0-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="a84c0-143">NOTES</span></span>

## <span data-ttu-id="a84c0-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a84c0-144">RELATED LINKS</span></span>
