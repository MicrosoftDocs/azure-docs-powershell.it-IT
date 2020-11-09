---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: cecfa3e009f6d6fbc7167c4b8f1ca110d547b5b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298680"
---
# <span data-ttu-id="ece14-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="ece14-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="ece14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ece14-102">SYNOPSIS</span></span>
<span data-ttu-id="ece14-103">Rimuove un utente in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ece14-103">Removes a user on a device.</span></span>

## <span data-ttu-id="ece14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ece14-104">SYNTAX</span></span>

### <span data-ttu-id="ece14-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ece14-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece14-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece14-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece14-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece14-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece14-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece14-108">DESCRIPTION</span></span>
<span data-ttu-id="ece14-109">Il cmdlet **Remove-AzDataBoxEdgeUser** rimuove un utente nel dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="ece14-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="ece14-110">È supportata la creazione di solo utenti di tipo `Share` .</span><span class="sxs-lookup"><span data-stu-id="ece14-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="ece14-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ece14-111">EXAMPLES</span></span>

### <span data-ttu-id="ece14-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ece14-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="ece14-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ece14-113">PARAMETERS</span></span>

### <span data-ttu-id="ece14-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ece14-114">-AsJob</span></span>
<span data-ttu-id="ece14-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ece14-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ece14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece14-116">-DefaultProfile</span></span>
<span data-ttu-id="ece14-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ece14-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ece14-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ece14-118">-DeviceName</span></span>
<span data-ttu-id="ece14-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="ece14-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece14-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ece14-120">-InputObject</span></span>
<span data-ttu-id="ece14-121">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="ece14-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ece14-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ece14-122">-Name</span></span>
<span data-ttu-id="ece14-123">Username</span><span class="sxs-lookup"><span data-stu-id="ece14-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece14-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ece14-124">-PassThru</span></span>
<span data-ttu-id="ece14-125">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="ece14-125">returns true if successful</span></span>

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

### <span data-ttu-id="ece14-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece14-126">-ResourceGroupName</span></span>
<span data-ttu-id="ece14-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ece14-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece14-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ece14-128">-ResourceId</span></span>
<span data-ttu-id="ece14-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ece14-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="ece14-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ece14-130">-Confirm</span></span>
<span data-ttu-id="ece14-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ece14-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece14-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece14-132">-WhatIf</span></span>
<span data-ttu-id="ece14-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ece14-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ece14-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ece14-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece14-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece14-135">CommonParameters</span></span>
<span data-ttu-id="ece14-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece14-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece14-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ece14-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece14-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ece14-138">INPUTS</span></span>

### <span data-ttu-id="ece14-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ece14-139">System.String</span></span>

### <span data-ttu-id="ece14-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="ece14-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="ece14-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ece14-141">OUTPUTS</span></span>

### <span data-ttu-id="ece14-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="ece14-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="ece14-143">Note</span><span class="sxs-lookup"><span data-stu-id="ece14-143">NOTES</span></span>

## <span data-ttu-id="ece14-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ece14-144">RELATED LINKS</span></span>
