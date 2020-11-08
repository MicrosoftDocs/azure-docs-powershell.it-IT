---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200659"
---
# <span data-ttu-id="a788d-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a788d-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="a788d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a788d-102">SYNOPSIS</span></span>
<span data-ttu-id="a788d-103">Imposta una nuova password per un utente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a788d-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="a788d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a788d-104">SYNTAX</span></span>

### <span data-ttu-id="a788d-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a788d-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a788d-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a788d-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a788d-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a788d-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a788d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a788d-108">DESCRIPTION</span></span>
<span data-ttu-id="a788d-109">Il cmdlet **set-AzStackEdgeUser** imposta una nuova password per un utente nel dispositivo stack Edge.</span><span class="sxs-lookup"><span data-stu-id="a788d-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="a788d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a788d-110">EXAMPLES</span></span>

### <span data-ttu-id="a788d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a788d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="a788d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a788d-112">PARAMETERS</span></span>

### <span data-ttu-id="a788d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a788d-113">-AsJob</span></span>
<span data-ttu-id="a788d-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a788d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a788d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a788d-115">-DefaultProfile</span></span>
<span data-ttu-id="a788d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a788d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a788d-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a788d-117">-DeviceName</span></span>
<span data-ttu-id="a788d-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="a788d-118">Device Name</span></span>

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

### <span data-ttu-id="a788d-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a788d-119">-EncryptionKey</span></span>
<span data-ttu-id="a788d-120">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="a788d-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="a788d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a788d-121">-InputObject</span></span>
<span data-ttu-id="a788d-122">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="a788d-122">Input Object</span></span>

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

### <span data-ttu-id="a788d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a788d-123">-Name</span></span>
<span data-ttu-id="a788d-124">Username</span><span class="sxs-lookup"><span data-stu-id="a788d-124">Username</span></span>

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

### <span data-ttu-id="a788d-125">-Password</span><span class="sxs-lookup"><span data-stu-id="a788d-125">-Password</span></span>
<span data-ttu-id="a788d-126">Password, specificare una stringa sicura</span><span class="sxs-lookup"><span data-stu-id="a788d-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="a788d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a788d-127">-ResourceGroupName</span></span>
<span data-ttu-id="a788d-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a788d-128">Resource Group Name</span></span>

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

### <span data-ttu-id="a788d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a788d-129">-ResourceId</span></span>
<span data-ttu-id="a788d-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a788d-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="a788d-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a788d-131">-Confirm</span></span>
<span data-ttu-id="a788d-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a788d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a788d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a788d-133">-WhatIf</span></span>
<span data-ttu-id="a788d-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a788d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a788d-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a788d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a788d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a788d-136">CommonParameters</span></span>
<span data-ttu-id="a788d-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a788d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a788d-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a788d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a788d-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a788d-139">INPUTS</span></span>

### <span data-ttu-id="a788d-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a788d-140">None</span></span>

## <span data-ttu-id="a788d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a788d-141">OUTPUTS</span></span>

### <span data-ttu-id="a788d-142">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a788d-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="a788d-143">Note</span><span class="sxs-lookup"><span data-stu-id="a788d-143">NOTES</span></span>

## <span data-ttu-id="a788d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a788d-144">RELATED LINKS</span></span>
