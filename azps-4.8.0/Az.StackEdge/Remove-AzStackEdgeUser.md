---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191166"
---
# <span data-ttu-id="65b96-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="65b96-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="65b96-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65b96-102">SYNOPSIS</span></span>
<span data-ttu-id="65b96-103">Rimuove un utente in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="65b96-103">Removes a user on a device.</span></span>

## <span data-ttu-id="65b96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65b96-104">SYNTAX</span></span>

### <span data-ttu-id="65b96-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="65b96-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b96-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65b96-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b96-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65b96-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65b96-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65b96-108">DESCRIPTION</span></span>
<span data-ttu-id="65b96-109">Il cmdlet **Remove-AzStackEdgeUser** rimuove un utente nel dispositivo dello stack Edge.</span><span class="sxs-lookup"><span data-stu-id="65b96-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="65b96-110">È supportata la creazione di solo utenti di tipo `Share` .</span><span class="sxs-lookup"><span data-stu-id="65b96-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="65b96-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65b96-111">EXAMPLES</span></span>

### <span data-ttu-id="65b96-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="65b96-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="65b96-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65b96-113">PARAMETERS</span></span>

### <span data-ttu-id="65b96-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65b96-114">-AsJob</span></span>
<span data-ttu-id="65b96-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="65b96-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65b96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b96-116">-DefaultProfile</span></span>
<span data-ttu-id="65b96-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65b96-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65b96-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="65b96-118">-DeviceName</span></span>
<span data-ttu-id="65b96-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="65b96-119">Device Name</span></span>

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

### <span data-ttu-id="65b96-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65b96-120">-InputObject</span></span>
<span data-ttu-id="65b96-121">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="65b96-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65b96-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="65b96-122">-Name</span></span>
<span data-ttu-id="65b96-123">Username</span><span class="sxs-lookup"><span data-stu-id="65b96-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b96-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65b96-124">-PassThru</span></span>
<span data-ttu-id="65b96-125">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="65b96-125">returns true if successful</span></span>

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

### <span data-ttu-id="65b96-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b96-126">-ResourceGroupName</span></span>
<span data-ttu-id="65b96-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="65b96-127">Resource Group Name</span></span>

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

### <span data-ttu-id="65b96-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65b96-128">-ResourceId</span></span>
<span data-ttu-id="65b96-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="65b96-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="65b96-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65b96-130">-Confirm</span></span>
<span data-ttu-id="65b96-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65b96-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65b96-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65b96-132">-WhatIf</span></span>
<span data-ttu-id="65b96-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65b96-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65b96-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65b96-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65b96-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b96-135">CommonParameters</span></span>
<span data-ttu-id="65b96-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b96-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b96-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65b96-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b96-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65b96-138">INPUTS</span></span>

### <span data-ttu-id="65b96-139">System. String</span><span class="sxs-lookup"><span data-stu-id="65b96-139">System.String</span></span>

### <span data-ttu-id="65b96-140">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="65b96-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="65b96-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65b96-141">OUTPUTS</span></span>

### <span data-ttu-id="65b96-142">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="65b96-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="65b96-143">Note</span><span class="sxs-lookup"><span data-stu-id="65b96-143">NOTES</span></span>

## <span data-ttu-id="65b96-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65b96-144">RELATED LINKS</span></span>
