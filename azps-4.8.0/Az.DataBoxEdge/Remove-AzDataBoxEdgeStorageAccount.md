---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 1f8e20b826a477778de5325ff147cbd7ad28a9fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192143"
---
# <span data-ttu-id="63256-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="63256-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="63256-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63256-102">SYNOPSIS</span></span>
<span data-ttu-id="63256-103">Consente di rimuovere l'account di archiviazione perimetrale per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63256-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="63256-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63256-104">SYNTAX</span></span>

### <span data-ttu-id="63256-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="63256-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63256-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63256-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63256-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63256-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63256-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63256-108">DESCRIPTION</span></span>
<span data-ttu-id="63256-109">Il cmdlet **Remove-AzDataBoxEdgeStorageAccount** rimuove un account di archiviazione Edge associato per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="63256-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="63256-110">È possibile specificare il nome dell'account di archiviazione Edge da rimuovere come parametro nel cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63256-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="63256-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63256-111">EXAMPLES</span></span>

### <span data-ttu-id="63256-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="63256-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="63256-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63256-113">PARAMETERS</span></span>

### <span data-ttu-id="63256-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63256-114">-AsJob</span></span>
<span data-ttu-id="63256-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="63256-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63256-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63256-116">-DefaultProfile</span></span>
<span data-ttu-id="63256-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63256-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63256-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="63256-118">-DeviceName</span></span>
<span data-ttu-id="63256-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="63256-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63256-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63256-120">-InputObject</span></span>
<span data-ttu-id="63256-121">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="63256-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63256-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="63256-122">-Name</span></span>
<span data-ttu-id="63256-123">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="63256-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63256-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63256-124">-PassThru</span></span>
<span data-ttu-id="63256-125">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="63256-125">returns true if successful</span></span>

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

### <span data-ttu-id="63256-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63256-126">-ResourceGroupName</span></span>
<span data-ttu-id="63256-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="63256-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63256-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63256-128">-ResourceId</span></span>
<span data-ttu-id="63256-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="63256-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63256-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="63256-130">-Confirm</span></span>
<span data-ttu-id="63256-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63256-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63256-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63256-132">-WhatIf</span></span>
<span data-ttu-id="63256-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63256-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63256-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63256-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63256-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63256-135">CommonParameters</span></span>
<span data-ttu-id="63256-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63256-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63256-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63256-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63256-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63256-138">INPUTS</span></span>

### <span data-ttu-id="63256-139">System. String</span><span class="sxs-lookup"><span data-stu-id="63256-139">System.String</span></span>

### <span data-ttu-id="63256-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="63256-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="63256-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63256-141">OUTPUTS</span></span>

### <span data-ttu-id="63256-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="63256-142">System.Boolean</span></span>

## <span data-ttu-id="63256-143">Note</span><span class="sxs-lookup"><span data-stu-id="63256-143">NOTES</span></span>

## <span data-ttu-id="63256-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63256-144">RELATED LINKS</span></span>
