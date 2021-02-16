---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176671"
---
# <span data-ttu-id="1b09d-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="1b09d-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="1b09d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b09d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b09d-103">Imposta una nuova password per un utente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b09d-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="1b09d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b09d-104">SYNTAX</span></span>

### <span data-ttu-id="1b09d-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b09d-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b09d-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b09d-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b09d-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b09d-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b09d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1b09d-108">DESCRIPTION</span></span>
<span data-ttu-id="1b09d-109">Il cmdlet **Set-AzStackEdgeUser** imposta una nuova password per un utente nel dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="1b09d-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="1b09d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b09d-110">EXAMPLES</span></span>

### <span data-ttu-id="1b09d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1b09d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="1b09d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b09d-112">PARAMETERS</span></span>

### <span data-ttu-id="1b09d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b09d-113">-AsJob</span></span>
<span data-ttu-id="1b09d-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1b09d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b09d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b09d-115">-DefaultProfile</span></span>
<span data-ttu-id="1b09d-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b09d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b09d-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1b09d-117">-DeviceName</span></span>
<span data-ttu-id="1b09d-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="1b09d-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b09d-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1b09d-119">-EncryptionKey</span></span>
<span data-ttu-id="1b09d-120">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="1b09d-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="1b09d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b09d-121">-InputObject</span></span>
<span data-ttu-id="1b09d-122">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="1b09d-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases: User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b09d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1b09d-123">-Name</span></span>
<span data-ttu-id="1b09d-124">Nome utente</span><span class="sxs-lookup"><span data-stu-id="1b09d-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b09d-125">-Password</span><span class="sxs-lookup"><span data-stu-id="1b09d-125">-Password</span></span>
<span data-ttu-id="1b09d-126">Password, fornisci come stringa sicura</span><span class="sxs-lookup"><span data-stu-id="1b09d-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="1b09d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b09d-127">-ResourceGroupName</span></span>
<span data-ttu-id="1b09d-128">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1b09d-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b09d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b09d-129">-ResourceId</span></span>
<span data-ttu-id="1b09d-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b09d-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b09d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b09d-131">-Confirm</span></span>
<span data-ttu-id="1b09d-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b09d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b09d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b09d-133">-WhatIf</span></span>
<span data-ttu-id="1b09d-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b09d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b09d-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b09d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b09d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b09d-136">CommonParameters</span></span>
<span data-ttu-id="1b09d-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b09d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b09d-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1b09d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b09d-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="1b09d-139">INPUTS</span></span>

### <span data-ttu-id="1b09d-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b09d-140">None</span></span>

## <span data-ttu-id="1b09d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b09d-141">OUTPUTS</span></span>

### <span data-ttu-id="1b09d-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="1b09d-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="1b09d-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="1b09d-143">NOTES</span></span>

## <span data-ttu-id="1b09d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b09d-144">RELATED LINKS</span></span>
