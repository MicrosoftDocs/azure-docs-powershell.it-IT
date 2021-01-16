---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349951"
---
# <span data-ttu-id="a0a18-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a0a18-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="a0a18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0a18-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a18-103">Imposta una nuova password per un utente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0a18-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="a0a18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0a18-104">SYNTAX</span></span>

### <span data-ttu-id="a0a18-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0a18-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0a18-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0a18-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0a18-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0a18-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0a18-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0a18-108">DESCRIPTION</span></span>
<span data-ttu-id="a0a18-109">Il cmdlet **set-AzStackEdgeUser** imposta una nuova password per un utente nel dispositivo stack Edge.</span><span class="sxs-lookup"><span data-stu-id="a0a18-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="a0a18-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0a18-110">EXAMPLES</span></span>

### <span data-ttu-id="a0a18-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0a18-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="a0a18-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0a18-112">PARAMETERS</span></span>

### <span data-ttu-id="a0a18-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0a18-113">-AsJob</span></span>
<span data-ttu-id="a0a18-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a0a18-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0a18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a18-115">-DefaultProfile</span></span>
<span data-ttu-id="a0a18-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0a18-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0a18-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a0a18-117">-DeviceName</span></span>
<span data-ttu-id="a0a18-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="a0a18-118">Device Name</span></span>

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

### <span data-ttu-id="a0a18-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a0a18-119">-EncryptionKey</span></span>
<span data-ttu-id="a0a18-120">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="a0a18-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="a0a18-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0a18-121">-InputObject</span></span>
<span data-ttu-id="a0a18-122">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="a0a18-122">Input Object</span></span>

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

### <span data-ttu-id="a0a18-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0a18-123">-Name</span></span>
<span data-ttu-id="a0a18-124">Username</span><span class="sxs-lookup"><span data-stu-id="a0a18-124">Username</span></span>

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

### <span data-ttu-id="a0a18-125">-Password</span><span class="sxs-lookup"><span data-stu-id="a0a18-125">-Password</span></span>
<span data-ttu-id="a0a18-126">Password, specificare una stringa sicura</span><span class="sxs-lookup"><span data-stu-id="a0a18-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="a0a18-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0a18-127">-ResourceGroupName</span></span>
<span data-ttu-id="a0a18-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a0a18-128">Resource Group Name</span></span>

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

### <span data-ttu-id="a0a18-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0a18-129">-ResourceId</span></span>
<span data-ttu-id="a0a18-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0a18-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="a0a18-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0a18-131">-Confirm</span></span>
<span data-ttu-id="a0a18-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0a18-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0a18-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a18-133">-WhatIf</span></span>
<span data-ttu-id="a0a18-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0a18-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0a18-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0a18-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0a18-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a18-136">CommonParameters</span></span>
<span data-ttu-id="a0a18-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0a18-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a18-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0a18-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a18-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0a18-139">INPUTS</span></span>

### <span data-ttu-id="a0a18-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a0a18-140">None</span></span>

## <span data-ttu-id="a0a18-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0a18-141">OUTPUTS</span></span>

### <span data-ttu-id="a0a18-142">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a0a18-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="a0a18-143">Note</span><span class="sxs-lookup"><span data-stu-id="a0a18-143">NOTES</span></span>

## <span data-ttu-id="a0a18-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0a18-144">RELATED LINKS</span></span>
