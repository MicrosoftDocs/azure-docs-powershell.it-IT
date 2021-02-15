---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: e1ebab6e0b32c6358defee30512185868581b6e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184838"
---
# <span data-ttu-id="e8ac0-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e8ac0-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="e8ac0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8ac0-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ac0-103">Crea un nuovo pool di file ANF (Azure NetApp).</span><span class="sxs-lookup"><span data-stu-id="e8ac0-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="e8ac0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8ac0-104">SYNTAX</span></span>

### <span data-ttu-id="e8ac0-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e8ac0-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ac0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8ac0-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8ac0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e8ac0-107">DESCRIPTION</span></span>
<span data-ttu-id="e8ac0-108">Il cmdlet **New-AzNetAppFilesPool** crea un pool ANF.</span><span class="sxs-lookup"><span data-stu-id="e8ac0-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="e8ac0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8ac0-109">EXAMPLES</span></span>

### <span data-ttu-id="e8ac0-110">Esempio 1: Creare un pool ANF</span><span class="sxs-lookup"><span data-stu-id="e8ac0-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium" -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="e8ac0-111">Questo comando crea il nuovo pool ANF "MyAnfPool" all'interno dell'account "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="e8ac0-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="e8ac0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8ac0-112">PARAMETERS</span></span>

### <span data-ttu-id="e8ac0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8ac0-113">-AccountName</span></span>
<span data-ttu-id="e8ac0-114">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="e8ac0-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac0-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="e8ac0-115">-AccountObject</span></span>
<span data-ttu-id="e8ac0-116">Account per il nuovo oggetto pool</span><span class="sxs-lookup"><span data-stu-id="e8ac0-116">The account for the new pool object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ac0-117">-DefaultProfile</span></span>
<span data-ttu-id="e8ac0-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ac0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8ac0-119">-Location</span><span class="sxs-lookup"><span data-stu-id="e8ac0-119">-Location</span></span>
<span data-ttu-id="e8ac0-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="e8ac0-120">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e8ac0-121">-Name</span></span>
<span data-ttu-id="e8ac0-122">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="e8ac0-122">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac0-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="e8ac0-123">-PoolSize</span></span>
<span data-ttu-id="e8ac0-124">Dimensioni del pool ANF</span><span class="sxs-lookup"><span data-stu-id="e8ac0-124">The size of the ANF pool</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac0-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="e8ac0-125">-QosType</span></span>
<span data-ttu-id="e8ac0-126">Il tipo di qos della pool.</span><span class="sxs-lookup"><span data-stu-id="e8ac0-126">The qos type of the pool.</span></span> <span data-ttu-id="e8ac0-127">I valori possibili includono" "Auto", "Manuale"</span><span class="sxs-lookup"><span data-stu-id="e8ac0-127">Possible values include: 'Auto', 'Manual'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Auto
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ac0-128">-ResourceGroupName</span></span>
<span data-ttu-id="e8ac0-129">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="e8ac0-129">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac0-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="e8ac0-130">-ServiceLevel</span></span>
<span data-ttu-id="e8ac0-131">Livello di servizio del pool ANF</span><span class="sxs-lookup"><span data-stu-id="e8ac0-131">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="e8ac0-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8ac0-132">-Tag</span></span>
<span data-ttu-id="e8ac0-133">Tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="e8ac0-133">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8ac0-134">-Confirm</span></span>
<span data-ttu-id="e8ac0-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8ac0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ac0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ac0-136">-WhatIf</span></span>
<span data-ttu-id="e8ac0-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8ac0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8ac0-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8ac0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ac0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ac0-139">CommonParameters</span></span>
<span data-ttu-id="e8ac0-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ac0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ac0-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e8ac0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ac0-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="e8ac0-142">INPUTS</span></span>

### <span data-ttu-id="e8ac0-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e8ac0-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="e8ac0-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8ac0-144">OUTPUTS</span></span>

### <span data-ttu-id="e8ac0-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e8ac0-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="e8ac0-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="e8ac0-146">NOTES</span></span>

## <span data-ttu-id="e8ac0-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8ac0-147">RELATED LINKS</span></span>
