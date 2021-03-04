---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: a2de03f28935fb8002966e0e9251218809ddec5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971277"
---
# <span data-ttu-id="5ccdd-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="5ccdd-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="5ccdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ccdd-102">SYNOPSIS</span></span>
<span data-ttu-id="5ccdd-103">Imposta una nuova password per un utente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5ccdd-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="5ccdd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ccdd-104">SYNTAX</span></span>

### <span data-ttu-id="5ccdd-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ccdd-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ccdd-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ccdd-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ccdd-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ccdd-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ccdd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5ccdd-108">DESCRIPTION</span></span>
<span data-ttu-id="5ccdd-109">Il cmdlet **Set-AzDataBoxEdgeUser** imposta una nuova password per un utente nel dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="5ccdd-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="5ccdd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ccdd-110">EXAMPLES</span></span>

### <span data-ttu-id="5ccdd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ccdd-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="5ccdd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ccdd-112">PARAMETERS</span></span>

### <span data-ttu-id="5ccdd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ccdd-113">-AsJob</span></span>
<span data-ttu-id="5ccdd-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5ccdd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ccdd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ccdd-115">-DefaultProfile</span></span>
<span data-ttu-id="5ccdd-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ccdd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ccdd-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5ccdd-117">-DeviceName</span></span>
<span data-ttu-id="5ccdd-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="5ccdd-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccdd-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5ccdd-119">-EncryptionKey</span></span>
<span data-ttu-id="5ccdd-120">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="5ccdd-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccdd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ccdd-121">-InputObject</span></span>
<span data-ttu-id="5ccdd-122">Oggetto input</span><span class="sxs-lookup"><span data-stu-id="5ccdd-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccdd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5ccdd-123">-Name</span></span>
<span data-ttu-id="5ccdd-124">Nome utente</span><span class="sxs-lookup"><span data-stu-id="5ccdd-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccdd-125">-Password</span><span class="sxs-lookup"><span data-stu-id="5ccdd-125">-Password</span></span>
<span data-ttu-id="5ccdd-126">Password, fornisci come stringa sicura</span><span class="sxs-lookup"><span data-stu-id="5ccdd-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccdd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ccdd-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ccdd-128">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5ccdd-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccdd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ccdd-129">-ResourceId</span></span>
<span data-ttu-id="5ccdd-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ccdd-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccdd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ccdd-131">-Confirm</span></span>
<span data-ttu-id="5ccdd-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ccdd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ccdd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ccdd-133">-WhatIf</span></span>
<span data-ttu-id="5ccdd-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ccdd-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ccdd-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ccdd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ccdd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ccdd-136">CommonParameters</span></span>
<span data-ttu-id="5ccdd-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ccdd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ccdd-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5ccdd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ccdd-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="5ccdd-139">INPUTS</span></span>

### <span data-ttu-id="5ccdd-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5ccdd-140">None</span></span>

## <span data-ttu-id="5ccdd-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ccdd-141">OUTPUTS</span></span>

### <span data-ttu-id="5ccdd-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="5ccdd-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="5ccdd-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="5ccdd-143">NOTES</span></span>

## <span data-ttu-id="5ccdd-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ccdd-144">RELATED LINKS</span></span>
