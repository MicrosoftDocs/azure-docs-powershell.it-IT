---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: 244adfb2707d47cef56390ce0d707b9f51fe229b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191782"
---
# <span data-ttu-id="c842f-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="c842f-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="c842f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c842f-102">SYNOPSIS</span></span>
<span data-ttu-id="c842f-103">Crea un nuovo utente per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c842f-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="c842f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c842f-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c842f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c842f-105">DESCRIPTION</span></span>
<span data-ttu-id="c842f-106">Il cmdlet **New-AzStackEdgeUser** crea un nuovo utente per il dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="c842f-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="c842f-107">È supportata la creazione di solo utenti di tipo `Share` .</span><span class="sxs-lookup"><span data-stu-id="c842f-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="c842f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c842f-108">EXAMPLES</span></span>

### <span data-ttu-id="c842f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c842f-109">Example 1</span></span>
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

## <span data-ttu-id="c842f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c842f-110">PARAMETERS</span></span>

### <span data-ttu-id="c842f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c842f-111">-AsJob</span></span>
<span data-ttu-id="c842f-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c842f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c842f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c842f-113">-DefaultProfile</span></span>
<span data-ttu-id="c842f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c842f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c842f-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c842f-115">-DeviceName</span></span>
<span data-ttu-id="c842f-116">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="c842f-116">Device Name</span></span>

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

### <span data-ttu-id="c842f-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c842f-117">-EncryptionKey</span></span>
<span data-ttu-id="c842f-118">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="c842f-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="c842f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c842f-119">-Name</span></span>
<span data-ttu-id="c842f-120">Username</span><span class="sxs-lookup"><span data-stu-id="c842f-120">Username</span></span>

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

### <span data-ttu-id="c842f-121">-Password</span><span class="sxs-lookup"><span data-stu-id="c842f-121">-Password</span></span>
<span data-ttu-id="c842f-122">Password, specificare una stringa sicura</span><span class="sxs-lookup"><span data-stu-id="c842f-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="c842f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c842f-123">-ResourceGroupName</span></span>
<span data-ttu-id="c842f-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c842f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c842f-125">-Digitare</span><span class="sxs-lookup"><span data-stu-id="c842f-125">-Type</span></span>
<span data-ttu-id="c842f-126">Selezionare UserType</span><span class="sxs-lookup"><span data-stu-id="c842f-126">Select UserType</span></span>

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

### <span data-ttu-id="c842f-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c842f-127">-Confirm</span></span>
<span data-ttu-id="c842f-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c842f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c842f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c842f-129">-WhatIf</span></span>
<span data-ttu-id="c842f-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c842f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c842f-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c842f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c842f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c842f-132">CommonParameters</span></span>
<span data-ttu-id="c842f-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c842f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c842f-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c842f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c842f-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c842f-135">INPUTS</span></span>

### <span data-ttu-id="c842f-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c842f-136">None</span></span>

## <span data-ttu-id="c842f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c842f-137">OUTPUTS</span></span>

### <span data-ttu-id="c842f-138">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c842f-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="c842f-139">Note</span><span class="sxs-lookup"><span data-stu-id="c842f-139">NOTES</span></span>

## <span data-ttu-id="c842f-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c842f-140">RELATED LINKS</span></span>
