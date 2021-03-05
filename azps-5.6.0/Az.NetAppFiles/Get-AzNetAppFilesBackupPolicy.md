---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: fc8e3d49f5c5a6430a6436b0d46e8fd10984db98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968622"
---
# <span data-ttu-id="88f2c-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="88f2c-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="88f2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="88f2c-103">Recupera i dettagli di un criterio di backup dei file ANF di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="88f2c-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="88f2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88f2c-104">SYNTAX</span></span>

### <span data-ttu-id="88f2c-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88f2c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88f2c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88f2c-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88f2c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88f2c-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88f2c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="88f2c-108">DESCRIPTION</span></span>
<span data-ttu-id="88f2c-109">Il **cmdlet Get-AzNetAppFilesBackupPolicy** ottiene i dettagli di un criterio di backup ANF.</span><span class="sxs-lookup"><span data-stu-id="88f2c-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="88f2c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88f2c-110">EXAMPLES</span></span>

### <span data-ttu-id="88f2c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="88f2c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="88f2c-112">Questo comando recupera il criterio di backup denominato "MyBackupPolicy" per l'account "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="88f2c-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="88f2c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88f2c-113">PARAMETERS</span></span>

### <span data-ttu-id="88f2c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="88f2c-114">-AccountName</span></span>
<span data-ttu-id="88f2c-115">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="88f2c-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="88f2c-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="88f2c-116">-AccountObject</span></span>
<span data-ttu-id="88f2c-117">Oggetto Account che contiene i criteri di backup da restituire</span><span class="sxs-lookup"><span data-stu-id="88f2c-117">The Account object containing the Backup Policy to return</span></span>

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

### <span data-ttu-id="88f2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f2c-118">-DefaultProfile</span></span>
<span data-ttu-id="88f2c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88f2c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88f2c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="88f2c-120">-Name</span></span>
<span data-ttu-id="88f2c-121">Nome dei criteri di backup ANF</span><span class="sxs-lookup"><span data-stu-id="88f2c-121">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="88f2c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88f2c-122">-ResourceGroupName</span></span>
<span data-ttu-id="88f2c-123">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="88f2c-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="88f2c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88f2c-124">-ResourceId</span></span>
<span data-ttu-id="88f2c-125">ID risorsa dei criteri di backup ANF</span><span class="sxs-lookup"><span data-stu-id="88f2c-125">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="88f2c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f2c-126">CommonParameters</span></span>
<span data-ttu-id="88f2c-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88f2c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f2c-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88f2c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f2c-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="88f2c-129">INPUTS</span></span>

### <span data-ttu-id="88f2c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="88f2c-130">System.String</span></span>

### <span data-ttu-id="88f2c-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="88f2c-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="88f2c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88f2c-132">OUTPUTS</span></span>

### <span data-ttu-id="88f2c-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="88f2c-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="88f2c-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="88f2c-134">NOTES</span></span>

## <span data-ttu-id="88f2c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88f2c-135">RELATED LINKS</span></span>
