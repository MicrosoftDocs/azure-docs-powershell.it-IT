---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 754149172b3154975580a0802426f9a2f20c0f62
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187278"
---
# <span data-ttu-id="9fbf0-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9fbf0-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="9fbf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbf0-103">Recupera i dettagli di un criterio di backup dei file ANF di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="9fbf0-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="9fbf0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fbf0-104">SYNTAX</span></span>

### <span data-ttu-id="9fbf0-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9fbf0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fbf0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fbf0-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fbf0-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fbf0-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fbf0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9fbf0-108">DESCRIPTION</span></span>
<span data-ttu-id="9fbf0-109">Il **cmdlet Get-AzNetAppFilesBackupPolicy** ottiene i dettagli di un criterio di backup ANF.</span><span class="sxs-lookup"><span data-stu-id="9fbf0-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="9fbf0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fbf0-110">EXAMPLES</span></span>

### <span data-ttu-id="9fbf0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9fbf0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="9fbf0-112">Questo comando recupera il criterio di backup denominato "MyBackupPolicy" per l'account "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="9fbf0-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="9fbf0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fbf0-113">PARAMETERS</span></span>

### <span data-ttu-id="9fbf0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9fbf0-114">-AccountName</span></span>
<span data-ttu-id="9fbf0-115">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="9fbf0-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="9fbf0-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="9fbf0-116">-AccountObject</span></span>
<span data-ttu-id="9fbf0-117">Oggetto Account che contiene i criteri di backup da restituire</span><span class="sxs-lookup"><span data-stu-id="9fbf0-117">The Account object containing the Backup Policy to return</span></span>

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

### <span data-ttu-id="9fbf0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbf0-118">-DefaultProfile</span></span>
<span data-ttu-id="9fbf0-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fbf0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fbf0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9fbf0-120">-Name</span></span>
<span data-ttu-id="9fbf0-121">Nome dei criteri di backup ANF</span><span class="sxs-lookup"><span data-stu-id="9fbf0-121">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="9fbf0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fbf0-122">-ResourceGroupName</span></span>
<span data-ttu-id="9fbf0-123">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="9fbf0-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9fbf0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fbf0-124">-ResourceId</span></span>
<span data-ttu-id="9fbf0-125">ID risorsa dei criteri di backup ANF</span><span class="sxs-lookup"><span data-stu-id="9fbf0-125">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="9fbf0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbf0-126">CommonParameters</span></span>
<span data-ttu-id="9fbf0-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fbf0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbf0-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9fbf0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbf0-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="9fbf0-129">INPUTS</span></span>

### <span data-ttu-id="9fbf0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9fbf0-130">System.String</span></span>

### <span data-ttu-id="9fbf0-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="9fbf0-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="9fbf0-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fbf0-132">OUTPUTS</span></span>

### <span data-ttu-id="9fbf0-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9fbf0-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="9fbf0-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="9fbf0-134">NOTES</span></span>

## <span data-ttu-id="9fbf0-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fbf0-135">RELATED LINKS</span></span>
