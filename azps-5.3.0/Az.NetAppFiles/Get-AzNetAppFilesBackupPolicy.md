---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 754149172b3154975580a0802426f9a2f20c0f62
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474020"
---
# <span data-ttu-id="b9bb8-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b9bb8-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="b9bb8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="b9bb8-103">Ottiene i dettagli dei criteri di backup di Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="b9bb8-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="b9bb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9bb8-104">SYNTAX</span></span>

### <span data-ttu-id="b9bb8-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9bb8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9bb8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9bb8-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9bb8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9bb8-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9bb8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9bb8-108">DESCRIPTION</span></span>
<span data-ttu-id="b9bb8-109">Il cmdlet **Get-AzNetAppFilesBackupPolicy** ottiene i dettagli di un criterio di backup di ANF.</span><span class="sxs-lookup"><span data-stu-id="b9bb8-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="b9bb8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9bb8-110">EXAMPLES</span></span>

### <span data-ttu-id="b9bb8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b9bb8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="b9bb8-112">Questo comando consente di ottenere i criteri di backup denominati "MyBackupPolicy" per l'account "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="b9bb8-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="b9bb8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9bb8-113">PARAMETERS</span></span>

### <span data-ttu-id="b9bb8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b9bb8-114">-AccountName</span></span>
<span data-ttu-id="b9bb8-115">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="b9bb8-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="b9bb8-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="b9bb8-116">-AccountObject</span></span>
<span data-ttu-id="b9bb8-117">Oggetto account che contiene i criteri di backup da restituire</span><span class="sxs-lookup"><span data-stu-id="b9bb8-117">The Account object containing the Backup Policy to return</span></span>

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

### <span data-ttu-id="b9bb8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9bb8-118">-DefaultProfile</span></span>
<span data-ttu-id="b9bb8-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9bb8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9bb8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9bb8-120">-Name</span></span>
<span data-ttu-id="b9bb8-121">Nome del criterio di backup di ANF</span><span class="sxs-lookup"><span data-stu-id="b9bb8-121">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9bb8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9bb8-122">-ResourceGroupName</span></span>
<span data-ttu-id="b9bb8-123">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="b9bb8-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b9bb8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9bb8-124">-ResourceId</span></span>
<span data-ttu-id="b9bb8-125">ID risorsa dei criteri di backup di ANF</span><span class="sxs-lookup"><span data-stu-id="b9bb8-125">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="b9bb8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9bb8-126">CommonParameters</span></span>
<span data-ttu-id="b9bb8-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9bb8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9bb8-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9bb8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9bb8-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9bb8-129">INPUTS</span></span>

### <span data-ttu-id="b9bb8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b9bb8-130">System.String</span></span>

### <span data-ttu-id="b9bb8-131">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b9bb8-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="b9bb8-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9bb8-132">OUTPUTS</span></span>

### <span data-ttu-id="b9bb8-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b9bb8-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="b9bb8-134">Note</span><span class="sxs-lookup"><span data-stu-id="b9bb8-134">NOTES</span></span>

## <span data-ttu-id="b9bb8-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9bb8-135">RELATED LINKS</span></span>
