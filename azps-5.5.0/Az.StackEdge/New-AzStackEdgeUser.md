---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: 244adfb2707d47cef56390ce0d707b9f51fe229b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187854"
---
# <span data-ttu-id="ac107-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="ac107-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="ac107-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac107-102">SYNOPSIS</span></span>
<span data-ttu-id="ac107-103">Crea un nuovo utente per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac107-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="ac107-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac107-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac107-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ac107-105">DESCRIPTION</span></span>
<span data-ttu-id="ac107-106">Il cmdlet **New-AzStackEdgeUser** crea un nuovo utente per il dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="ac107-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="ac107-107">È supportata la creazione solo di `Share` utenti di tipo.</span><span class="sxs-lookup"><span data-stu-id="ac107-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="ac107-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac107-108">EXAMPLES</span></span>

### <span data-ttu-id="ac107-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ac107-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="ac107-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac107-110">PARAMETERS</span></span>

### <span data-ttu-id="ac107-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac107-111">-AsJob</span></span>
<span data-ttu-id="ac107-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ac107-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac107-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac107-113">-DefaultProfile</span></span>
<span data-ttu-id="ac107-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac107-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac107-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ac107-115">-DeviceName</span></span>
<span data-ttu-id="ac107-116">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="ac107-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac107-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ac107-117">-EncryptionKey</span></span>
<span data-ttu-id="ac107-118">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="ac107-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="ac107-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ac107-119">-Name</span></span>
<span data-ttu-id="ac107-120">Nome utente</span><span class="sxs-lookup"><span data-stu-id="ac107-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac107-121">-Password</span><span class="sxs-lookup"><span data-stu-id="ac107-121">-Password</span></span>
<span data-ttu-id="ac107-122">Password, fornisci come stringa sicura</span><span class="sxs-lookup"><span data-stu-id="ac107-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="ac107-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac107-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac107-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ac107-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac107-125">-Type</span><span class="sxs-lookup"><span data-stu-id="ac107-125">-Type</span></span>
<span data-ttu-id="ac107-126">Selezionare UserType</span><span class="sxs-lookup"><span data-stu-id="ac107-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac107-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac107-127">-Confirm</span></span>
<span data-ttu-id="ac107-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac107-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac107-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac107-129">-WhatIf</span></span>
<span data-ttu-id="ac107-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac107-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac107-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac107-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac107-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac107-132">CommonParameters</span></span>
<span data-ttu-id="ac107-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac107-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac107-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac107-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac107-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ac107-135">INPUTS</span></span>

### <span data-ttu-id="ac107-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ac107-136">None</span></span>

## <span data-ttu-id="ac107-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac107-137">OUTPUTS</span></span>

### <span data-ttu-id="ac107-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ac107-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="ac107-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="ac107-139">NOTES</span></span>

## <span data-ttu-id="ac107-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac107-140">RELATED LINKS</span></span>
