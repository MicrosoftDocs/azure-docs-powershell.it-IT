---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: 58ae996e4d2723d4b38b548dd8225a2a483ce8f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177695"
---
# <span data-ttu-id="14846-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="14846-101">New-AzHost</span></span>

## <span data-ttu-id="14846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14846-102">SYNOPSIS</span></span>
<span data-ttu-id="14846-103">Crea un host.</span><span class="sxs-lookup"><span data-stu-id="14846-103">Creates a  host.</span></span>

## <span data-ttu-id="14846-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14846-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14846-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14846-105">DESCRIPTION</span></span>
<span data-ttu-id="14846-106">Questo cmdlet creerà un host.</span><span class="sxs-lookup"><span data-stu-id="14846-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="14846-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14846-107">EXAMPLES</span></span>

### <span data-ttu-id="14846-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14846-108">Example 1</span></span>
```
PS C:\> New-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -Location $location -Sku $skuName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 0
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
ProvisioningTime     : 7/25/2019 8:34:16 PM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="14846-109">Questo comando crea un host della SKU specificata nel gruppo host specificato e nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="14846-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="14846-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14846-110">PARAMETERS</span></span>

### <span data-ttu-id="14846-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14846-111">-AsJob</span></span>
<span data-ttu-id="14846-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="14846-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14846-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="14846-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="14846-114">Specifica se l'host deve essere sostituito automaticamente in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="14846-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="14846-115">Il valore predefinito è "true" se non viene fornito.</span><span class="sxs-lookup"><span data-stu-id="14846-115">The value is defaulted to 'true' when not provided.</span></span>

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

### <span data-ttu-id="14846-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14846-116">-DefaultProfile</span></span>
<span data-ttu-id="14846-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14846-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14846-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="14846-118">-HostGroupName</span></span>
<span data-ttu-id="14846-119">Specifica il nome del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="14846-119">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="14846-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="14846-120">-LicenseType</span></span>
<span data-ttu-id="14846-121">Specifica il tipo di licenza software che verrà applicato alle macchine virtuali distribuite nell'host.</span><span class="sxs-lookup"><span data-stu-id="14846-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="14846-122">I valori possibili sono: Nessuno, Windows_Server_Hybrid e Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="14846-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="14846-123">Il valore predefinito è Nessuno.</span><span class="sxs-lookup"><span data-stu-id="14846-123">Default value is None.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DedicatedHostLicenseTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, WindowsServerHybrid, WindowsServerPerpetual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14846-124">-Location</span><span class="sxs-lookup"><span data-stu-id="14846-124">-Location</span></span>
<span data-ttu-id="14846-125">Specifica la posizione.</span><span class="sxs-lookup"><span data-stu-id="14846-125">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14846-126">-Name</span><span class="sxs-lookup"><span data-stu-id="14846-126">-Name</span></span>
<span data-ttu-id="14846-127">Specifica il nome dell'host.</span><span class="sxs-lookup"><span data-stu-id="14846-127">Specifies the name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14846-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="14846-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="14846-129">Specifica il numero di dominio di errore della piattaforma dell'host.</span><span class="sxs-lookup"><span data-stu-id="14846-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="14846-130">Il valore minimo è quindi 0 e il valore massimo è 2.</span><span class="sxs-lookup"><span data-stu-id="14846-130">Then minimum value is 0 and the maximum value is 2.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14846-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14846-131">-ResourceGroupName</span></span>
<span data-ttu-id="14846-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14846-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="14846-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="14846-133">-Sku</span></span>
<span data-ttu-id="14846-134">Specifica il nome dello SKU.</span><span class="sxs-lookup"><span data-stu-id="14846-134">Specifies the name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14846-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="14846-135">-Tag</span></span>
<span data-ttu-id="14846-136">Specifica tag.</span><span class="sxs-lookup"><span data-stu-id="14846-136">Specifies Tags.</span></span>

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

### <span data-ttu-id="14846-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14846-137">-Confirm</span></span>
<span data-ttu-id="14846-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14846-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14846-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14846-139">-WhatIf</span></span>
<span data-ttu-id="14846-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14846-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14846-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14846-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14846-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14846-142">CommonParameters</span></span>
<span data-ttu-id="14846-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14846-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14846-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14846-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14846-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="14846-145">INPUTS</span></span>

### <span data-ttu-id="14846-146">System.String</span><span class="sxs-lookup"><span data-stu-id="14846-146">System.String</span></span>

## <span data-ttu-id="14846-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14846-147">OUTPUTS</span></span>

### <span data-ttu-id="14846-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="14846-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="14846-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="14846-149">NOTES</span></span>

## <span data-ttu-id="14846-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14846-150">RELATED LINKS</span></span>
