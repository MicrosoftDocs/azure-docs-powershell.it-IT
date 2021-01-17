---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: b65bfc61b354a5a45ac009b40b54de46d94ef56c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474015"
---
# <span data-ttu-id="9c956-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="9c956-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="9c956-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c956-102">SYNOPSIS</span></span>
<span data-ttu-id="9c956-103">Ottiene i dettagli dei criteri di snapshot di un file di Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="9c956-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="9c956-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c956-104">SYNTAX</span></span>

### <span data-ttu-id="9c956-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c956-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c956-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c956-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c956-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c956-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c956-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c956-108">DESCRIPTION</span></span>
<span data-ttu-id="9c956-109">Il cmdlet **Get-AzNetAppFilesSnapshotPolicy** ottiene i dettagli di un criterio di snapshot di ANF.</span><span class="sxs-lookup"><span data-stu-id="9c956-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="9c956-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c956-110">EXAMPLES</span></span>

### <span data-ttu-id="9c956-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9c956-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="9c956-112">Questo comando consente di ottenere i criteri di backup denominati "MyBackupPolicy" per l'account "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="9c956-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="9c956-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c956-113">PARAMETERS</span></span>

### <span data-ttu-id="9c956-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9c956-114">-AccountName</span></span>
<span data-ttu-id="9c956-115">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="9c956-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c956-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="9c956-116">-AccountObject</span></span>
<span data-ttu-id="9c956-117">Account per il nuovo oggetto Criteri snapshot</span><span class="sxs-lookup"><span data-stu-id="9c956-117">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c956-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c956-118">-DefaultProfile</span></span>
<span data-ttu-id="9c956-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c956-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c956-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c956-120">-Name</span></span>
<span data-ttu-id="9c956-121">Nome dei criteri di snapshot di ANF</span><span class="sxs-lookup"><span data-stu-id="9c956-121">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c956-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c956-122">-ResourceGroupName</span></span>
<span data-ttu-id="9c956-123">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="9c956-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c956-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c956-124">-ResourceId</span></span>
<span data-ttu-id="9c956-125">ID risorsa dei criteri di snapshot di ANF</span><span class="sxs-lookup"><span data-stu-id="9c956-125">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c956-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c956-126">-Confirm</span></span>
<span data-ttu-id="9c956-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c956-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c956-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c956-128">-WhatIf</span></span>
<span data-ttu-id="9c956-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c956-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c956-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c956-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c956-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c956-131">CommonParameters</span></span>
<span data-ttu-id="9c956-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c956-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c956-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c956-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c956-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c956-134">INPUTS</span></span>

### <span data-ttu-id="9c956-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9c956-135">System.String</span></span>

### <span data-ttu-id="9c956-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="9c956-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="9c956-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c956-137">OUTPUTS</span></span>

### <span data-ttu-id="9c956-138">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="9c956-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="9c956-139">Note</span><span class="sxs-lookup"><span data-stu-id="9c956-139">NOTES</span></span>

## <span data-ttu-id="9c956-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c956-140">RELATED LINKS</span></span>
