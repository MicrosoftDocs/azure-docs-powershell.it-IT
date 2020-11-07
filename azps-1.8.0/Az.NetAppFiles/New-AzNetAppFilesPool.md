---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: fdadfde6c798bf404d1f99dbb1ff2a8109d41f73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678733"
---
# <span data-ttu-id="5b59f-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5b59f-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="5b59f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b59f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b59f-103">Crea un nuovo pool di file di ANF (Azure NetApp files).</span><span class="sxs-lookup"><span data-stu-id="5b59f-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="5b59f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b59f-104">SYNTAX</span></span>

### <span data-ttu-id="5b59f-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b59f-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b59f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b59f-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b59f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b59f-107">DESCRIPTION</span></span>
<span data-ttu-id="5b59f-108">Il cmdlet **New-AzNetAppFilesPool** crea un pool di ANF.</span><span class="sxs-lookup"><span data-stu-id="5b59f-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="5b59f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b59f-109">EXAMPLES</span></span>

### <span data-ttu-id="5b59f-110">Esempio 1: creare un pool di ANF</span><span class="sxs-lookup"><span data-stu-id="5b59f-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="5b59f-111">Questo comando crea il nuovo pool di ANF "MyAnfPool" nell'account "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="5b59f-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="5b59f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b59f-112">PARAMETERS</span></span>

### <span data-ttu-id="5b59f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5b59f-113">-AccountName</span></span>
<span data-ttu-id="5b59f-114">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="5b59f-114">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b59f-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="5b59f-115">-AccountObject</span></span>
<span data-ttu-id="5b59f-116">Account per il nuovo oggetto pool</span><span class="sxs-lookup"><span data-stu-id="5b59f-116">The account for the new pool object</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b59f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b59f-117">-DefaultProfile</span></span>
<span data-ttu-id="5b59f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b59f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b59f-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5b59f-119">-Location</span></span>
<span data-ttu-id="5b59f-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="5b59f-120">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b59f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b59f-121">-Name</span></span>
<span data-ttu-id="5b59f-122">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="5b59f-122">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b59f-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="5b59f-123">-PoolSize</span></span>
<span data-ttu-id="5b59f-124">Dimensioni del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="5b59f-124">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b59f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b59f-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b59f-126">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="5b59f-126">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b59f-127">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="5b59f-127">-ServiceLevel</span></span>
<span data-ttu-id="5b59f-128">Livello di servizio del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="5b59f-128">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="5b59f-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b59f-129">-Tag</span></span>
<span data-ttu-id="5b59f-130">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="5b59f-130">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b59f-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b59f-131">-Confirm</span></span>
<span data-ttu-id="5b59f-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b59f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b59f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b59f-133">-WhatIf</span></span>
<span data-ttu-id="5b59f-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b59f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b59f-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b59f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b59f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b59f-136">CommonParameters</span></span>
<span data-ttu-id="5b59f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b59f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5b59f-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b59f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b59f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b59f-139">INPUTS</span></span>

### <span data-ttu-id="5b59f-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5b59f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="5b59f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b59f-141">OUTPUTS</span></span>

### <span data-ttu-id="5b59f-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5b59f-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="5b59f-143">Note</span><span class="sxs-lookup"><span data-stu-id="5b59f-143">NOTES</span></span>

## <span data-ttu-id="5b59f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b59f-144">RELATED LINKS</span></span>