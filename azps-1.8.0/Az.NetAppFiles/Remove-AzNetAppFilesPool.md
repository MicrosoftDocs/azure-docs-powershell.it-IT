---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: ef896185b606e107bb62208255a255655814fcbc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678722"
---
# <span data-ttu-id="acf45-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="acf45-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="acf45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="acf45-102">SYNOPSIS</span></span>
<span data-ttu-id="acf45-103">Elimina un pool di file ANF (Azure NetApp files).</span><span class="sxs-lookup"><span data-stu-id="acf45-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="acf45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acf45-104">SYNTAX</span></span>

### <span data-ttu-id="acf45-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="acf45-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf45-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acf45-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf45-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acf45-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf45-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acf45-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acf45-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acf45-109">DESCRIPTION</span></span>
<span data-ttu-id="acf45-110">Il cmdlet **Remove-AzNetAppFilesPool** Elimina un pool di ANF.</span><span class="sxs-lookup"><span data-stu-id="acf45-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="acf45-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acf45-111">EXAMPLES</span></span>

### <span data-ttu-id="acf45-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="acf45-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="acf45-113">Questo comando Elimina il pool di ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="acf45-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="acf45-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="acf45-114">PARAMETERS</span></span>

### <span data-ttu-id="acf45-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="acf45-115">-AccountName</span></span>
<span data-ttu-id="acf45-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="acf45-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="acf45-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="acf45-117">-AccountObject</span></span>
<span data-ttu-id="acf45-118">Oggetto account che contiene il pool da rimuovere</span><span class="sxs-lookup"><span data-stu-id="acf45-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="acf45-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf45-119">-DefaultProfile</span></span>
<span data-ttu-id="acf45-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acf45-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf45-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acf45-121">-InputObject</span></span>
<span data-ttu-id="acf45-122">Oggetto pool da rimuovere</span><span class="sxs-lookup"><span data-stu-id="acf45-122">The pool object to remove</span></span>

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

### <span data-ttu-id="acf45-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="acf45-123">-Name</span></span>
<span data-ttu-id="acf45-124">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="acf45-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="acf45-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="acf45-125">-PassThru</span></span>
<span data-ttu-id="acf45-126">Restituisce se il pool specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="acf45-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="acf45-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf45-127">-ResourceGroupName</span></span>
<span data-ttu-id="acf45-128">Gruppo risorse del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="acf45-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="acf45-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acf45-129">-ResourceId</span></span>
<span data-ttu-id="acf45-130">ID risorsa del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="acf45-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="acf45-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="acf45-131">-Confirm</span></span>
<span data-ttu-id="acf45-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acf45-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acf45-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf45-133">-WhatIf</span></span>
<span data-ttu-id="acf45-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acf45-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf45-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acf45-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acf45-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf45-136">CommonParameters</span></span>
<span data-ttu-id="acf45-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acf45-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="acf45-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acf45-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf45-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="acf45-139">INPUTS</span></span>

### <span data-ttu-id="acf45-140">System. String</span><span class="sxs-lookup"><span data-stu-id="acf45-140">System.String</span></span>

### <span data-ttu-id="acf45-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="acf45-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="acf45-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="acf45-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="acf45-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acf45-143">OUTPUTS</span></span>

### <span data-ttu-id="acf45-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="acf45-144">System.Boolean</span></span>

## <span data-ttu-id="acf45-145">Note</span><span class="sxs-lookup"><span data-stu-id="acf45-145">NOTES</span></span>

## <span data-ttu-id="acf45-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acf45-146">RELATED LINKS</span></span>