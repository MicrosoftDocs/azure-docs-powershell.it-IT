---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 717c1cac6def6fb51f1ab8b598f15a05a7d62db4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864186"
---
# <span data-ttu-id="78d34-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="78d34-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="78d34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78d34-102">SYNOPSIS</span></span>
<span data-ttu-id="78d34-103">Elimina un pool di file ANF (Azure NetApp files).</span><span class="sxs-lookup"><span data-stu-id="78d34-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="78d34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78d34-104">SYNTAX</span></span>

### <span data-ttu-id="78d34-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78d34-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d34-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78d34-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d34-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78d34-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d34-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78d34-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d34-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78d34-109">DESCRIPTION</span></span>
<span data-ttu-id="78d34-110">Il cmdlet **Remove-AzNetAppFilesPool** Elimina un pool di ANF.</span><span class="sxs-lookup"><span data-stu-id="78d34-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="78d34-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78d34-111">EXAMPLES</span></span>

### <span data-ttu-id="78d34-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="78d34-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="78d34-113">Questo comando Elimina il pool di ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="78d34-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="78d34-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78d34-114">PARAMETERS</span></span>

### <span data-ttu-id="78d34-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78d34-115">-AccountName</span></span>
<span data-ttu-id="78d34-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="78d34-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="78d34-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="78d34-117">-AccountObject</span></span>
<span data-ttu-id="78d34-118">Oggetto account che contiene il pool da rimuovere</span><span class="sxs-lookup"><span data-stu-id="78d34-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="78d34-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d34-119">-DefaultProfile</span></span>
<span data-ttu-id="78d34-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78d34-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78d34-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78d34-121">-InputObject</span></span>
<span data-ttu-id="78d34-122">Oggetto pool da rimuovere</span><span class="sxs-lookup"><span data-stu-id="78d34-122">The pool object to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78d34-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="78d34-123">-Name</span></span>
<span data-ttu-id="78d34-124">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="78d34-124">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d34-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78d34-125">-PassThru</span></span>
<span data-ttu-id="78d34-126">Restituisce se il pool specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="78d34-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="78d34-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d34-127">-ResourceGroupName</span></span>
<span data-ttu-id="78d34-128">Gruppo risorse del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="78d34-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="78d34-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78d34-129">-ResourceId</span></span>
<span data-ttu-id="78d34-130">ID risorsa del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="78d34-130">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d34-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="78d34-131">-Confirm</span></span>
<span data-ttu-id="78d34-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d34-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d34-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d34-133">-WhatIf</span></span>
<span data-ttu-id="78d34-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78d34-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d34-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78d34-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d34-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d34-136">CommonParameters</span></span>
<span data-ttu-id="78d34-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d34-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="78d34-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78d34-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d34-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78d34-139">INPUTS</span></span>

### <span data-ttu-id="78d34-140">System. String</span><span class="sxs-lookup"><span data-stu-id="78d34-140">System.String</span></span>

### <span data-ttu-id="78d34-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="78d34-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="78d34-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="78d34-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="78d34-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78d34-143">OUTPUTS</span></span>

### <span data-ttu-id="78d34-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78d34-144">System.Boolean</span></span>

## <span data-ttu-id="78d34-145">Note</span><span class="sxs-lookup"><span data-stu-id="78d34-145">NOTES</span></span>

## <span data-ttu-id="78d34-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78d34-146">RELATED LINKS</span></span>
